````markdown
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

Écrire un message sur son téléphone pendant la marche modifie-t-il l'intensité du mouvement ?

### Hypothèse

L'utilisation du téléphone pendant la marche entraîne une diminution de l'intensité du mouvement, observable par une diminution de l'ENMO moyen.

## 2. Protocole expérimental

Trois participants ont réalisé deux conditions expérimentales :

- **Condition 1 :** marche normale pendant 2 minutes
- **Condition 2 :** marche pendant 2 minutes en écrivant un message sur un téléphone

Les mesures ont été enregistrées à l'aide d'un accéléromètre Axivity AX3 fixé à la cheville droite.

Trois frappes du pied au début de chaque condition ont permis de repérer le début de la période expérimentale (on observe des pics très élevés sur les graphiques d'ENMO).

## 3. Méthode d'analyse

Les données d'accélération sont enregistrées sur trois axes (X, Y et Z).

La variable étudiée est l'ENMO (*Euclidean Norm Minus One*), exprimée en milli-g (mg) :

ENMO = max(√(X² + Y² + Z²) − 1, 0) × 1000

L'analyse comprend :
- La vérification de la qualité des données brutes.
- Le calcul de l'ENMO.
- La sélection de la période de marche (2 minutes), en retirant les 10 premières et les 10 dernières secondes pour éliminer les frappes du pied et les phases de démarrage et d'arrêt. On analyse donc 100 secondes de marche par condition.
- Le calcul de l'ENMO moyen par fenêtres de 10 secondes (10 fenêtres par condition).
- La comparaison des deux conditions pour chaque participant (graphiques, boxplots, variation en %).
- Un test de Mann-Whitney pour vérifier si la différence entre les deux conditions est significative (p < 0,05).
- Le calcul de la cadence de marche (pas par minute), à partir des pics d'accélération à la cheville, pour vérifier si la baisse de l'ENMO s'accompagne d'un ralentissement de la marche.

## 4. Principaux résultats

Les trois participants présentent une diminution de l'ENMO moyen lorsqu'ils écrivent un message sur leur téléphone en marchant :

| Participant | Sans téléphone (mg) | Avec téléphone (mg) | Variation ENMO (%) | p (Mann-Whitney) | Variation cadence (%) |
|---|---|---|---|---|---|
| Tania | 582,75 | 356,91 | −38,75 | 0,0002 | −16,7 |
| Thomas | 426,85 | 396,56 | −7,10 | 0,0058 | −1,1 |
| Sarah | 504,34 | 347,30 | −31,14 | 0,0002 | −8,3 |

La diminution moyenne de l'ENMO est de −25,66 %, et elle est significative pour les trois participants (p < 0,05).

La cadence diminue également, et dans le même ordre que l'ENMO : une partie de la baisse d'intensité semble donc liée à un ralentissement de la marche lors de l'utilisation du téléphone.

## 5. Conclusion

Nos résultats vont dans le sens de notre hypothèse : écrire un message en marchant diminue l'intensité du mouvement. L'effet varie cependant beaucoup d'une personne à l'autre (de −7 % à −39 %), et ces différences suivent celles de la cadence.

### Limites

- **Faible nombre de participants** (n = 3) : les résultats ne peuvent pas être généralisés.
- **Vitesse de marche non mesurée directement** : la cadence donne une indication, mais la longueur des pas et la vitesse n'ont pas été mesurées.
- **Fenêtres non indépendantes** : le test de Mann-Whitney compare des fenêtres de 10 s issues d'une même marche, qui ne sont pas totalement indépendantes ; les p-valeurs sont donc à interpréter avec prudence.
- **Comparaison avec la littérature** : le capteur a été placé à la cheville, ce qui a permis de calculer la cadence. En contrepartie, nos valeurs d'ENMO ne peuvent pas être comparées directement aux seuils d'intensité publiés, établis pour des capteurs portés au poignet ou à la hanche (Hildebrand et al., 2014).

## 6. Organisation du dépôt

```text
HAH913E-2026-Projet-C/
│
├── README.md
├── main.ipynb   # notebook principal (analyse des trois participants)
│
├── notebooks/
│   ├── README.md
│   ├── Analyse_données_tania_(sujet-1).ipynb
│   ├── Analyse_données_thomas_(sujet-2).ipynb
│   └── Analyse_données_sarah_(sujet-3).ipynb
│
├── data/
│   ├── README.md
│   └── fichiers CSV (Tania, Thomas, Sarah : sans et avec téléphone)
│
└── results/
    ├── README.md
    ├── synthese_ENMO.csv
    └── figures/
```

## 7. Installation et utilisation

### Prérequis

- Python 3
- Jupyter Notebook ou JupyterLab (ou VS Code)
- Bibliothèques : numpy, pandas, matplotlib, scipy

### Exécution du projet

1. Cloner le dépôt GitHub.
2. Ouvrir le dossier du projet dans Jupyter Notebook.
3. Ouvrir `main.ipynb`.
4. Exécuter toutes les cellules dans l'ordre avec **Run All**.

Le notebook principal permet de reproduire les analyses des trois participants et de générer les tableaux et graphiques associés.

## Référence

Hildebrand M, van Hees VT, Hansen BH, Ekelund U. Age group comparability of raw accelerometer output from wrist- and hip-worn monitors. *Medicine & Science in Sports & Exercise*. 2014;46(9):1816-1824. doi:10.1249/MSS.0000000000000289

---

Projet réalisé dans le cadre de l'UE HAH913E – Physical Activity for Health.
````