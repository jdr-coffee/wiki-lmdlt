---
title: Comment contribuer au wiki
description: Toutes les façons de participer à l'amélioration du wiki de Le Mythe de la Taverne.
---

Ce wiki est collaboratif. Si tu repères une erreur, une info manquante, ou que tu veux enrichir une page, tu es la bienvenue.

## La voie rapide — par Discord

Pas envie de toucher à GitHub ? Pas de problème. Le plus simple c'est de passer par le Discord.

1. Rejoins le serveur Discord : **[discord.gg/KuB3mxe3aX](https://discord.gg/KuB3mxe3aX)**
2. Rends-toi dans la catégorie **Le Wiki**, salon **[#contributions-wiki](https://discord.com/channels/1068521764814065786/1291809852015902731)**
3. Décris ce que tu voudrais ajouter ou corriger en mentionnant **@Tomo**, qui s'occupe de la gestion du wiki

C'est la voie recommandée pour une correction ponctuelle ou une petite suggestion.

## La voie autonome — Obsidian + GitHub Desktop

Pour celles et ceux qui veulent modifier le wiki directement, voici le protocole. Ça demande un peu de mise en place la première fois, mais c'est accessible même sans expérience technique.

### Ce dont tu as besoin

- Un compte **GitHub** (gratuit) : [github.com](https://github.com)
- **GitHub Desktop** : une application qui permet de gérer le wiki sans ligne de commande — [desktop.github.com](https://desktop.github.com)
- **Obsidian** : l'éditeur avec lequel le wiki est écrit — [obsidian.md](https://obsidian.md)

### Étape 1 — Forker le repo

"Forker" veut dire créer ta propre copie personnelle du wiki sur GitHub. C'est sur cette copie que tu vas travailler — le wiki officiel reste intact.

1. Va sur [github.com/jdr-coffee/wiki-lmdlt](https://github.com/jdr-coffee/wiki-lmdlt)
2. Clique sur le bouton **Fork** en haut à droite
3. Laisse les options par défaut et confirme

Tu as maintenant ton propre exemplaire du wiki sur ton compte GitHub.

### Étape 2 — Cloner le repo sur ton ordinateur

"Cloner" veut dire télécharger le wiki sur ton ordinateur pour pouvoir l'éditer.

1. Ouvre **GitHub Desktop**
2. Va dans **File → Clone repository**
3. Sélectionne le fork que tu viens de créer (il apparaît dans la liste)
4. Choisis où tu veux enregistrer les fichiers sur ton ordinateur, puis clique **Clone**

### Étape 3 — Ouvrir le wiki dans Obsidian

1. Ouvre **Obsidian**
2. Clique sur **Ouvrir un dossier comme coffre**
3. Navigue jusqu'au dossier que tu as cloné et sélectionne-le **tel quel** (pas le sous-dossier `wiki/`, mais bien le dossier racine du repo)

> **Pourquoi pas le dossier `wiki/` directement ?** Obsidian a besoin de voir l'ensemble du repo pour que les listes de pages (bases) fonctionnent correctement. Le contenu que tu modifies se trouve bien dans `wiki/`, mais le coffre doit pointer sur le dossier parent.

Tu peux maintenant naviguer dans toutes les pages et les modifier comme un document texte normal.

### Étape 4 — Faire tes modifications

Modifie les pages existantes ou crée-en de nouvelles directement dans Obsidian. Quelques règles à respecter :

- Ne pas modifier les faits établis de l'univers sans en avoir discuté avec Tomo au préalable
- Pour la mise en forme, s'inspirer des pages existantes — elles servent de référence pour le style et la structure
- Les noms de fichiers en minuscules avec des tirets (ex: `mon-personnage.md`)
- Pas besoin d'ajouter de titre en début de page — il est généré automatiquement

### Étape 5 — Enregistrer et envoyer tes modifications

Dans GitHub Desktop, tu verras la liste de ce que tu as modifié.

1. En bas à gauche, écris un court résumé de ce que tu as fait (ex: *"Ajout de la section historique sur Chelinka"*)
2. Clique sur **Commit to main**
3. Clique sur **Push origin** pour envoyer tes modifications sur ton fork GitHub

### Étape 6 — Proposer tes modifications (Pull Request)

C'est la dernière étape : tu proposes tes modifications à Tomo pour qu'il les intègre au wiki officiel.

1. Sur GitHub Desktop, clique sur **Create Pull Request** — ça ouvre une page dans ton navigateur
2. Ajoute un titre et une courte description de ce que tu as fait
3. Clique sur **Create pull request**

Tomo recevra une notification, relira tes modifications et les intégrera au wiki officiel (ou te demandera des ajustements si besoin).

N'hésite pas à ping **@Tomo** sur le Discord une fois ta PR ouverte, ou à tout moment si tu as une question en cours de route — salon [#contributions-wiki](https://discord.com/channels/1068521764814065786/1291809852015902731).
