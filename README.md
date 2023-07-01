# *La "marque" du lieu dans le "quartier Richelieu"*: conférence à Humanistica 2023, Genève

Ce dépôt contient les sources des *slides* et de l'*abstract* publié dans les actes du colloque Humanistica à Genève.

---

## Abstract

À partir d'un corpus complexe (iconographique, cartographique, textuel) portant 
sur un quartier parisien (1750-1950), nous proposons de définir un élément à même 
de réunir, de modéliser et de représenter nos sources : le lieu. Celui-ci permet 
de faire converger les composantes spatiales et historiques de notre corpus. Il 
s'agit alors de montrer la manière dont le lieu est appréhendé d'un point de vue 
technique : de quelle manière il peut être modélisé, mais aussi comment il peut 
être représenté dans un modèle 3D historique. Enfin, nous présenterons la manière 
dont le lieu peut servir de moteur pour l'exploration et l'interaction avec le 
corpus sur une application Web. En définitive, nous souhaitons interroger la 
manière dont le lieu vient modifier notre rapport aux sources et à la technique, 
dans le cadre d'un projet en humanités numériques et en histoire de l'architecture. 

---

## Compiler les sources

Cloner le dépôt:

```bash
git clone https://github.com/paulhectork/humanistica2023.git
cd humanistica2023
```

Compiler l'article: utiliser **pdflatex**
```bash
cd article
pdflatex -synctex=1 -interaction=nonstopmode humanistica_abstract_230627.tex
biber ./humanistica_abstract_230627.aux
pdflatex -synctex=1 -interaction=nonstopmode humanistica_abstract_230627.tex
pdflatex -synctex=1 -interaction=nonstopmode humanistica_abstract_230627.tex
```

Compiler les slides: utiliser **xelatex** (compiler 2 fois si besoin)
```bash
xelatex -synctex=1 -shell-escape -interaction=nonstopmode -8bit "humanistica_slides_230627".tex
```

---

## Remerciements

Les auteurices remercient Simon Gabay (@gabays) pour ses conseils, relectures et précieux débuggages du code LaTeX et de ses bugs sans fin.

---

## Citation

```bibtex
@inproceedings{kervegan:hal-04108218,
  TITLE = {{`` La marque du lieu '' dans le `` quartier Richelieu ''}},
  AUTHOR = {Kervegan, Paul and Duvette, Charlotte and Jeanson, Lo{\"i}c and Prudhomme, Colin and Gain, Justine and Dasilva, Esther and Baranger, Louise},
  URL = {https://hal.science/hal-04108218},
  BOOKTITLE = {{Humanistica 2023}},
  ADDRESS = {Gen{\`e}ve, Switzerland},
  ORGANIZATION = {{Association francophone des humanit{\'e}s num{\'e}riques}},
  SERIES = {G{\'e}ographie},
  YEAR = {2023},
  MONTH = Jun,
  KEYWORDS = {Paris ; History of cities ; Iconography ; Cartography ; Cartographie ; Paris ; Histoire de la ville ; Iconographie},
  PDF = {https://hal.science/hal-04108218/file/Humanistica_2023_kervegan.pdf},
  HAL_ID = {hal-04108218},
  HAL_VERSION = {v1},
}
```
