# Diagramme de Séquence

Ce diagramme détaille les interactions temporelles entre l'utilisateur, le système et la base de données lors du scénario principal : **"Réserver un bureau"**.

```mermaid
sequenceDiagram
    actor U as Utilisateur
    participant S as Système (FlexiDesk)
    participant B as Base de Données

    Note over U, B: Scénario : Recherche et Réservation d'un espace

    %% Étape 1 : Recherche
    U->>S: 1. Sélectionne Date et Heure
    S->>B: 2. Requête disponibilité (date, heure)
    B-->>S: 3. Retourne liste des bureaux libres
    S-->>U: 4. Affiche les résultats

    %% Étape 2 : Réservation
    U->>S: 5. Clique sur "Réserver" (Bureau #42)
    S->>B: 6. Vérification finale & Enregistrement
    
    alt Succès (Bureau libre)
        B-->>S: 7. Confirmation enregistrée
        S-->>U: 8. Affiche "Réservation confirmée !"
        S-->>U: 9. Envoie email de confirmation
    else Échec (Bureau pris entre-temps)
        B-->>S: 7. Erreur (Conflit)
        S-->>U: 8. Affiche "Désolé, ce bureau vient d'être réservé."
    end
