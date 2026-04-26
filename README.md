# PHP Tech Watch

Veille technologique quotidienne autour de **PHP**, **Symfony** et **DevOps**, générée automatiquement chaque matin par une GitHub Action.

## Fonctionnement

```
Flux RSS → GitHub Action (daybrief) → Résumé Gemini AI → Email newsletter
```

Le workflow tourne tous les jours à 7h00 UTC via `yoanbernabeu/daybrief`.  
Les newsletters générées sont archivées dans le dossier `output/`.

## Configuration

Les sources RSS, la langue et le ton éditorial sont définis dans [`config.yaml`](./config.yaml).

## Secrets GitHub requis

À configurer dans **Settings → Secrets and variables → Actions** :

| Secret | Description |
|---|---|
| `GEMINI_API_KEY` | Clé API Google AI Studio (gratuit) |
| `SMTP_HOST` | Serveur SMTP (ex: `smtp.gmail.com`) |
| `SMTP_PORT` | Port SMTP (ex: `587`) |
| `SMTP_USERNAME` | Adresse email expéditeur |
| `SMTP_PASSWORD` | Mot de passe ou App Password Gmail |
| `MAIL_FROM_NAME` | Nom affiché de l'expéditeur |
| `MAIL_FROM_EMAIL` | Adresse email affiché de l'expéditeur |
| `DAYBRIEF_RECIPIENTS` | Destinataires, séparés par des virgules |
| `YOUTUBE_API_KEY` | *(optionnel)* Clé YouTube Data API v3 |

## Lancer manuellement

Dans l'onglet **Actions** du dépôt GitHub → workflow **DayBrief Newsletter** → **Run workflow**.

## Sources suivies

- PHP.net, PHP Foundation, PHP.Watch, Stitcher.io, Freek.dev, PHP Architect
- Symfony Blog, SymfonyStation
- Laravel News
- The New Stack, Martin Fowler, Docker Blog, Kubernetes Blog
- Dev.to (tags : php, symfony, devops)

## Références

- [yoanbernabeu/daybrief](https://github.com/yoanbernabeu/daybrief) — action utilisée
- [Google AI Studio](https://aistudio.google.com/) — clé Gemini gratuite
