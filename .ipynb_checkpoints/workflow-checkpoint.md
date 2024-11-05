# Le processus de Data Science

Le processus en science des données suit une série d’étapes, chacune étant conçue pour assurer la qualité et la fiabilité des résultats finaux. La clarté des objectifs, la rigueur dans la collecte et la préparation des données, ainsi qu'une analyse soignée garantissent le succès d’un projet. Chacune de ces étapes est détaillée ci-dessous.

---

## Définition du problème

Définir le problème avec précision est crucial, car un problème mal défini risque de conduire à des analyses inutiles ou erronées. Cette étape permet d’orienter le travail vers un objectif clair, en évitant les dérives. Il ne suffit pas de vouloir "analyser des données" : il faut savoir **ce que l’on veut accomplir**, pourquoi cela est important, et comment les résultats seront utilisés.

Il est également fondamental de bien comprendre le **contexte métier**. La manière dont un problème est formulé diffère selon le secteur. Par exemple, une entreprise de marketing pourrait chercher à améliorer les taux de conversion, tandis qu’un hôpital pourrait vouloir optimiser les soins à partir des dossiers patients.

---

### Identifier clairement l’objectif du projet

Chaque projet doit se concentrer sur un ou plusieurs objectifs bien définis. Un objectif clair permet de guider l’analyse et d’éviter de perdre du temps à explorer des pistes non pertinentes. Il aide aussi à fixer des métriques de performance précises, comme le taux de churn ou la précision d’un modèle prédictif.

```{admonition} Exemple : Objectif d’un projet d’analyse des ventes
Le but est de prédire les produits les plus vendus pendant la période de Noël. Cela permettra à l’équipe de logistique d’optimiser le stock et d’éviter des ruptures pendant cette période critique.
```

---

### Déterminer les questions auxquelles on veut répondre

Définir les bonnes questions à poser est tout aussi important que l’objectif. Ces questions orienteront la sélection des données et des outils d’analyse à utiliser. En répondant à ces questions, le scientifique des données peut s’assurer que l’analyse produira un impact mesurable et utile.

```{admonition} Exemple : Questions pour prédire le churn
1. Quels sont les facteurs qui influencent le désabonnement des clients ?
2. Les clients avec une faible activité récente sont-ils plus susceptibles de partir ?
3. Y a-t-il une corrélation entre le type de produit acheté et le taux de churn ?
```

---

## Collecte des données

L’analyse de données ne peut se faire qu’à partir de **données pertinentes et de bonne qualité**. Il est essentiel d’identifier les sources les plus adaptées en fonction de l’objectif du projet. La qualité des résultats dépend largement de la qualité des données collectées.

### Identifier les sources de données pertinentes

Les sources peuvent être internes (systèmes d’information de l’entreprise) ou externes (open data, réseaux sociaux, APIs). Identifier la source correcte permet d’assurer que les données collectées répondent aux besoins spécifiques du projet.

```{admonition} Exemple : Sources pour une analyse de comportement d’achat
1. Données de transactions provenant du site e-commerce.
2. Informations sur les visites de clients dans les magasins physiques.
3. Réseaux sociaux pour analyser les avis des consommateurs.
```

### Rassembler les données nécessaires

Une fois les sources identifiées, il faut **intégrer les données** en un format exploitable. Cette étape est cruciale, surtout si les données proviennent de plusieurs systèmes ou formats. Il peut être nécessaire d’écrire des scripts pour collecter des données automatiquement via des APIs ou d’accéder à des bases SQL pour extraire des informations.

---

## Nettoyage et préparation des données

Les données collectées sont souvent imparfaites, avec des **valeurs manquantes, des doublons ou des erreurs**. Le nettoyage garantit que les analyses seront fiables et non biaisées par des données incorrectes ou incomplètes.

### Traiter les données manquantes ou incorrectes

Les **valeurs manquantes** sont courantes dans les bases de données : certaines informations peuvent être mal saisies, oubliées, ou indisponibles. Laisser ces valeurs non traitées peut biaiser les résultats ou même empêcher certains algorithmes de fonctionner. Plusieurs stratégies sont possibles :
1. **Suppression** : Si peu de lignes sont affectées, il est parfois préférable de supprimer ces lignes.
2. **Imputation** : Remplacement des valeurs manquantes par une estimation (comme la moyenne ou la médiane). L’imputation réduit la perte d’informations mais peut introduire un biais.

Il est important de choisir la méthode en fonction du contexte. Par exemple, remplacer toutes les valeurs manquantes par la moyenne peut fausser des tendances si les données sont très dispersées.

```{admonition} Exemple : Traitement des données manquantes  
| Client_ID | Date d'achat | Montant (€) |
|-----------|--------------|-------------|
| 1         | 2023-10-01   | 150         |
| 2         |              | 200         |
| 3         | 2023-09-15   |             |

- **Imputer la date manquante** avec la date moyenne des achats précédents.
- **Remplacer le montant manquant** par la médiane des transactions similaires.
```

### Formater les données pour l’analyse

Avant l’analyse, les données doivent être **normalisées et mises en forme**. Cela implique souvent :
- **Conversion des types de données** : Par exemple, transformer des dates en objets datetime pour faciliter l’analyse chronologique.
- **Normalisation des valeurs** : Mettre les variables sur la même échelle pour que certaines variables ne dominent pas les autres dans les modèles. Cela est particulièrement important pour les algorithmes sensibles aux échelles, comme les k-means ou les régressions logistiques.

La **normalisation** consiste généralement à ramener les valeurs dans une plage [0,1] ou à les centrer autour de la moyenne avec un écart-type de 1. Cela permet d'éviter que des variables ayant des unités différentes (par exemple, euros et kilomètres) influencent de manière disproportionnée les résultats.

```{admonition} Exemple : Normalisation d’une variable
Supposons un ensemble de données contenant des informations sur le prix et le poids d’articles.

| Produit | Prix (€) | Poids (kg) |
|---------|----------|------------|
| A       | 100      | 1          |
| B       | 250      | 2.5        |
| C       | 300      | 3          |

Après normalisation :  
- Prix : $ (x - \mu) / \sigma $  
- Poids : $ (x - \mu) / \sigma $

Résultat :  

| Produit | Prix normalisé | Poids normalisé |
|---------|----------------|-----------------|
| A       | -1.14          | -1.22           |
| B       | 0.57           | 0.00            |
| C       | 0.57           | 1.22            |
```


