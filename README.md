# Guide d'utilisation des slides avec MARP

## Qu'est-ce que MARP ?

MARP (Markdown Presentation Ecosystem) est un outil qui permet de créer des présentations élégantes en utilisant uniquement du Markdown. Il transforme vos fichiers Markdown en présentations HTML, PDF ou PPTX.

## Installation

### Extension VS Code

La méthode la plus simple est d'utiliser l'extension VS Code :

1. Ouvrez VS Code
2. Allez dans Extensions (Ctrl+Shift+X)
3. Recherchez "Marp for VS Code"
4. Installez l'extension

### CLI (ligne de commande)

```bash
npm install -g @marp-team/marp-cli
```

## Créer une présentation

### Configuration de base

Commencez votre fichier Markdown avec un front matter YAML :

```markdown
---
marp: true
theme: default
paginate: true
---

# Ma première présentation avec MARP

## Sous-titre
```

### Séparation des slides

Pour créer une nouvelle diapositive, utilisez `---` :

```markdown
# Première diapositive

Contenu

---

# Deuxième diapositive

Contenu
```

## Personnalisation

### Thèmes disponibles

```markdown
---
theme: default | gaia | uncover
---
```

### Styles personnalisés

```markdown
---
style: |
  section {
      background-color: #f5f5f5;
  }
---
```

### Images

```markdown
![width:500px](image.jpg)
![bg](background.jpg)
![bg right:40%](image-right.jpg)
```

## Exportation

### Avec l'extension VS Code

1. Ouvrez la prévisualisation (Ctrl+Shift+V)
2. Cliquez sur l'icône d'exportation
3. Choisissez le format (PDF, PPTX, HTML)

### Avec le CLI

```bash
marp --pdf presentation.md
marp --pptx presentation.md
marp --html presentation.md
```

## Astuces avancées

- Utiliser `<!-- _class: lead -->` pour une mise en page centrée
- Ajouter `<!-- _footer: Mon pied de page -->` pour des pieds de page spécifiques
- Utiliser `<!-- _backgroundColor: #123456 -->` pour changer la couleur de fond d'une diapositive

## Ressources

- [Documentation officielle](https://marpit.marp.app/)
- [GitHub Marp Core](https://github.com/marp-team/marp-core)
- [Marp CLI](https://github.com/marp-team/marp-cli)
