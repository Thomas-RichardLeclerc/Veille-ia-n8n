```mermaid
flowchart LR
    A[Déclencheur 7h] --> B[Liste des sources]
    B --> C[Lecture RSS]
    C --> D[Filtre date]
    D --> E[Filtre pertinence]
    E --> F[Regroupement]
    F --> G[Résumé par Gemini]
    G --> H[Envoi Discord]
    C -. erreur .-> I[Alerte source]
```
