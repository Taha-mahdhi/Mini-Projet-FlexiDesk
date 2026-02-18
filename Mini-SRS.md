# Mini-SRS : Système de Réservation FlexiDesk

## 1. Introduction
**But du projet** : Ce document spécifie les exigences pour "FlexiDesk", une application web permettant aux travailleurs indépendants de réserver des espaces de travail en temps réel.
**Public cible** : Freelances, équipes distantes et administrateurs d'espaces de coworking.

## 2. Besoins Fonctionnels

### 2.1 Gestion des Utilisateurs
* Le système doit permettre aux utilisateurs de créer un compte (Freelance ou Entreprise).
* Le système doit sécuriser l'authentification via email et mot de passe.

### 2.2 Réservation et Recherche
* L'utilisateur doit pouvoir filtrer les bureaux par : date, équipement (ex: double écran) et localisation.
* Le système doit empêcher la double réservation d'un même bureau sur le même créneau horaire.
* L'utilisateur doit recevoir une confirmation immédiate après la réservation.

### 2.3 Administration
* L'administrateur doit pouvoir ajouter, modifier ou supprimer des bureaux de l'inventaire.
* L'administrateur doit avoir une vue d'ensemble des taux d'occupation.

---

## 3. Backlog Produit (User Stories)

| ID | En tant que... | Je veux... | Afin de... | Priorité |
|:---|:---|:---|:---|:---|
| **US-01** | Freelance | Voir un calendrier des disponibilités | Choisir mes jours de travail à l'avance | Haute |
| **US-02** | Freelance | Recevoir une notification de confirmation | Avoir une preuve de ma réservation | Moyenne |
| **US-03** | Admin | Mettre un bureau "Hors Service" | Empêcher les réservations pendant la maintenance | Haute |

---

## 4. Exigences Non-Fonctionnelles
1. **Performance** : L'affichage des résultats de recherche ne doit pas dépasser 2 secondes.
2. **Disponibilité** : Le service doit être accessible 24h/24 et 7j/7.
3. **Sécurité** : Les données de paiement et mots de passe doivent être chiffrés.

---

## 5. Modélisation
*Les diagrammes (Cas d'utilisation et Séquence) et les maquettes sont stockés dans les dossiers correspondants du dépôt Git.*
