# wiki-lmdlt

Repo de données du wiki **Le Mythe de la Taverne**.

Ce repo est la source de contenu pour [moulin](https://github.com/tomo/moulin) — l'app Next.js qui rend le wiki en production. Le contenu est du Markdown standard (CommonMark + extensions GFM), éditable dans n'importe quel éditeur — Obsidian, VS Code, ou tout autre outil Markdown. Synchronisé via git.

## Structure

```
wiki-lmdlt/
├── wiki/           ← vault Obsidian (contenu éditorial)
│   ├── _theme.yaml ← couleurs du thème (accent, etc.)
│   ├── index.md    ← page d'accueil
│   ├── episodes/
│   ├── personnages/
│   └── ...
└── README.md
```

Le dossier `wiki/` est la **production éditoriale**. Le format est volontairement générique — Markdown standard avec quelques extensions documentées dans [moulin/specs/SYNTAX.md](https://github.com/tomo/moulin/blob/main/specs/SYNTAX.md). Ne pas modifier à la main sauf pour les fichiers de config (`_theme.yaml`, `_collection.yaml`, `index.md` avec `::collection`).

## Fichiers de config dans `wiki/`

| Fichier | Rôle |
|---------|------|
| `_theme.yaml` | Couleurs OKLch du wiki (accent, accent_foreground) |
| `_collection.yaml` | Configuration d'affichage d'un dossier (vue, tri, groupement) |

Ces fichiers **survivent à la migration** (le script ne les écrase pas).

## Déploiement

En production (Vercel), moulin clone ce repo au build via la variable `CONTENT_REPO_URL`.

## Dev local

Cloner ce repo, puis définir dans `apps/web/.env.local` de moulin :

```bash
CONTENT_DIR=/chemin/vers/wiki-lmdlt/wiki
```

## Migration depuis Notion

Si une nouvelle export Notion est disponible :

```bash
node scripts/migrate-notion.mjs "/chemin/export/Wiki - Le Mythe de la Taverne" /chemin/vers/wiki-lmdlt/wiki
```

⚠️ La migration **écrase tout le contenu** de `wiki/` sauf `_theme.yaml`. Les `_collection.yaml` et `index.md` personnalisés sont à reconfigurer après.
