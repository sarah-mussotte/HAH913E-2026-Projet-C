# HAH913E-2026-Projet-C
Physical Activity Projet C

# Influence de l'utilisation du téléphone sur le mouvement pendant la marche

**UE : HAH913E – Physical Activity for Health**

**Année universitaire : 2026-2027**

**Membres du groupe :** Tania Faraj, Thomas Vigneau-Sugar et Sarah Mussotte.

---

## 1. Présentation du projet

L'utilisation du téléphone portable pendant la marche est devenue une pratique courante. Pourtant, cette activité implique de réaliser simultanément une tâche motrice et une tâche cognitive, ce qui pourrait modifier le comportement locomoteur.

Ce projet vise à étudier l'influence de l'utilisation du téléphone pendant la marche sur l'intensité du mouvement, à partir de données d'accélérométrie.

### Problématique

L'utilisation du téléphone pendant la marche modifie-t-elle l'intensité du mouvement ?

### Hypothèse

L'utilisation du téléphone pendant la marche entraîne une diminution de l'intensité du mouvement, observable par une diminution de l'ENMO moyen.

## 2. Protocole expérimental

Trois participants ont réalisé deux conditions expérimentales :

- **Condition 1 :** marche normale pendant 2 minutes
- **Condition 2 :** marche pendant 2 minutes en écrivant un message sur un téléphone

Les mesures ont été enregistrées à l'aide d'un accéléromètre Axivity AX3 fixé à la cheville droite.

Trois frappes du pied au début de chaque condition ont permis de repérer le début de la période expérimentale (on observe des pics très élevés sur les graphique d'ENMO).

## 3. Méthode d'analyse

Les données d'accélération sont enregistrées sur trois axes (X, Y et Z).

L'indicateur utilisé est l'ENMO (*Euclidean Norm Minus One*), exprimé en milli-g (mg).

Il est calculé selon la formule :

ENMO = max(√(X² + Y² + Z²) − 1, 0) × 1000

L'analyse comprend :
- La vérification de la qualité des données brutes.
- Le calcul de l'ENMO.
- La visualisation des signaux d'accélération.
- Le calcul de l'ENMO moyen par fenêtres de 10 secondes sur la période de marche réelle.
- La comparaison entre les deux conditions expérimentales.

## 4. Principaux résultats

Les trois participants présentent une diminution de l'ENMO moyen lors de la marche sur leur téléphone en écrivant un message.

![Comparaison de l'ENMO](results/figures/Graphiques_comparatifs/Comparaison_collective_ENMO_moyen.png)

La diminution relative observée est de :
- Tania : −38,75 %.
- Thomas : −7,10 %.
- Sarah : −31,14 %.

La diminution moyenne descriptive des trois participants est d'environ 27,29 %.

Ces résultats suggèrent une modification de l'intensité du mouvement pendant l'utilisation du téléphone. Ils doivent cependant être interprétés avec prudence compte tenu du faible nombre de participants.

## 5. Organisation du dépôt

```text
HAH913E-2026-Projet-C/
│
├── README.md
├── main.ipynb  #notebook principal
├── requirements.txt
│
├── notebooks/
│   ├── README.md
│   ├── Analyse_Tania.ipynb
│   ├── Analyse_Thomas.ipynb
│   └── Analyse_Sarah.ipynb
│
├── data/
│   ├── README.md
│   └── fichiers CSV
│
└── results/
    ├── README.md
    ├── figures/
    └── resultats_analyse.pdf
```

## 6. Installation et utilisation

### Prérequis

- Python 3
- Jupyter Notebook ou JupyterLab

### Exécution du projet

1. Cloner le dépôt GitHub.
2. Ouvrir le dossier du projet dans Jupyter Notebook.
3. Ouvrir `main.ipynb`.
4. Exécuter toutes les cellules dans l'ordre avec **Run All**.

Le notebook principal permet de reproduire les analyses des trois participants et de générer les tableaux et graphiques associés.


Projet réalisé dans le cadre de l'UE HAH913E – Physical Activity for Health.
