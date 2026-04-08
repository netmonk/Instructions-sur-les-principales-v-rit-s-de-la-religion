# Construction du PDF sous Linux

Ce dépôt contient le document LaTeX `instructions.tex`.
La compilation produit le fichier `instructions.pdf`.

## Prérequis

Installer une distribution LaTeX avec les paquets utilisés par le document :

- `extbook`
- `babel` avec le support français
- `kpfonts`
- `geometry`
- `titling`
- `subfiles`

Sous Debian / Ubuntu, le plus simple est d'installer :

```bash
sudo apt update
sudo apt install texlive-latex-extra texlive-fonts-extra texlive-lang-french
```

## Compiler le PDF

Depuis la racine du dépôt :

```bash
pdflatex instructions.tex
pdflatex instructions.tex
```

Deux passes sont recommandées pour générer correctement la table des matières.

Le PDF final est écrit dans :

```text
instructions.pdf
```

## Nettoyage

Pour supprimer les fichiers intermédiaires :

```bash
rm -f instructions.aux instructions.log instructions.toc
```
