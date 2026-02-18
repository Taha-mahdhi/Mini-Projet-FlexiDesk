

## 1. Diagramme de Cas d'Utilisation (DCU)
**Objectif** : Identifier les acteurs et leurs interactions avec le système.

```mermaid
graph LR
    %% Acteurs
    U[Freelance / User]
    A[Administrateur]

    %% Système
    subgraph Système_FlexiDesk
        direction TB
        UC1((S'authentifier))
        UC2((Rechercher un bureau))
        UC3((Réserver un créneau))
        UC4((Gérer les ressources))
        UC5((Consulter le planning))
    end

    %% Relations
    U --> UC1
    U --> UC2
    U --> UC3
    
    A --> UC1
    A --> UC4
    A --> UC5
