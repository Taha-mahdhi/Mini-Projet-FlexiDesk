# Modèle du Domaine (Diagramme de Classes)

Ce diagramme représente la structure statique du système FlexiDesk, y compris les entités principales et leurs relations.

```mermaid
classDiagram
    %% Relations
    Utilisateur "1" --> "0..*" Reservation : effectue
    Ressource "1" --> "0..*" Reservation : est_réservée_dans

    %% Classes
    class Utilisateur {
        +Int id
        +String nom
        +String email
        +String motDePasse
        +login()
        +logout()
    }

    class Ressource {
        +Int id
        +String type
        +Float prix
        +Boolean estLibre
        +definirDisponibilite()
    }

    class Reservation {
        +Int id
        +Date date
        +Heure debut
        +Heure fin
        +confirmer()
        +annuler()
    }
