# Instructions sur les principales vérités de la Religion

Ce dépôt contient la source LaTeX du livre
`Instructions sur les principales vérités de la Religion, et sur les principaux devoirs du christianisme`,
dans son édition de `1833`.

L'ouvrage est attribué à l'`Abbé HUMBERT`, aussi désigné dans la notice biographique comme le
`P. Humbert` ou `Hubert Humbert`, missionnaire du diocèse de Besançon né vers `1685/1686` et mort
en `1778`.

Le document principal est [`instructions.tex`](instructions.tex). Il assemble la page de titre,
la table des matières, une notice sur l'auteur et les différents chapitres du livre.

## Fabriquer le PDF sous Linux

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
