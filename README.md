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

## Convention titre

Le titre d'une page est déterminé dans cet ordre :
1. `title` en frontmatter — pour les cas spéciaux (accents, acronymes, noms propres)
2. Nom du fichier prettifié — `chelinka.md` → "Chelinka", `livre-de-base.md` → "Livre de base"

**Pas de H1 dans les fichiers markdown** — le titre est injecté automatiquement par moulin au render.

## Fichiers de config dans `wiki/`

| Fichier | Rôle |
|---------|------|
| `_theme.yaml` | Couleurs OKLch du wiki (accent, accent_foreground) |
| `*.base` | Configuration d'affichage d'un dossier (vue, tri, groupement — format Obsidian Bases) |

Ces fichiers **survivent à la migration** (le script ne les écrase pas).

## Déploiement

En production (Vercel), moulin clone ce repo au build via la variable `CONTENT_REPO_URL`.

## Dev local

Cloner ce repo, puis définir dans `.env.local` de moulin :

```bash
CONTENT_DIR=/chemin/vers/wiki-lmdlt/wiki
```

## Migration depuis Notion

Si une nouvelle export Notion est disponible :

```bash
node scripts/migrate-notion.mjs "/chemin/export/Wiki - Le Mythe de la Taverne" /chemin/vers/wiki-lmdlt/wiki
```

⚠️ La migration **écrase tout le contenu** de `wiki/`. Les fichiers `.base` et `index.md` personnalisés sont à reconfigurer après.
