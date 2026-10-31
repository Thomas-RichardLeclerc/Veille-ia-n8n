# Veille IA automatisée

Un workflow n8n qui lit des flux RSS chaque matin, filtre les articles pertinents, les fait résumer par un modèle de langage et envoie le digest sur Discord.

![Exemple de digest reçu sur Discord](docs/digest-discord.png)

## Architecture

```mermaid
flowchart TD
    A1[Déclencheur horaire 7h] --> B[Liste des sources]
    A2[Déclenchement manuel] --> B
    B --> C[Lecture RSS]
    C --> D[Filtre date]
    D --> E[Filtre pertinence]
    E --> F[Regroupement]
    F --> G[Résumé par Gemini]
    G --> H[Envoi Discord]
    C -. en cas d'erreur .-> I[Alerte source]
    style I fill:#ffe0cc,stroke:#cc6600
```
