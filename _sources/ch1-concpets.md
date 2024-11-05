# Chapitre 2 : Concepts Clés de l'IA

## Apprentissage Automatique (Machine Learning)
L’apprentissage automatique permet aux systèmes d’évoluer à partir de données.


:::{admonition} Apprentissage Supervisé : Concept et Applications

L'apprentissage supervisé est une technique de **Machine Learning** où un modèle est entraîné à partir de **données étiquetées**. Les données étiquetées signifient que pour chaque entrée, la sortie correcte (ou le label) est déjà connue. Le but du modèle est de **trouver une relation entre les entrées et les sorties** afin de faire des **prédictions sur des données nouvelles** ou inconnues.

Par exemple, si nous avons un ensemble de données contenant des e-mails étiquetés comme "spam" ou "non-spam", l'objectif du modèle sera d'apprendre à **classer correctement de nouveaux e-mails** en fonction de ces catégories.

:::

:::{admonition} Caractéristiques de l'apprentissage supervisé

1. **Données étiquetées** : Chaque exemple d'entraînement possède une entrée (caractéristiques) et une sortie connue (label).
2. **Entraînement du modèle** : Le modèle apprend à partir des erreurs faites pendant l'entraînement en ajustant ses paramètres.
3. **Évaluation de la performance** : Le modèle est évalué sur des données de test pour vérifier s'il peut bien généraliser à de nouveaux cas.
4. **Minimisation de l'erreur** : L’objectif est de réduire l’écart entre la sortie prédite et la sortie réelle.

:::

:::{admonition} Applications de l'apprentissage supervisé

1. Classification d’e-mails : Spam ou Non-Spam  
    - **Description** : Le modèle apprend à distinguer les e-mails indésirables (spam) des e-mails normaux en fonction de leur contenu.
    - **Entrée** : E-mail (texte, adresses, objets).
    - **Sortie** : "Spam" ou "Non-Spam".
    - **Exemple** : Si un e-mail contient des mots comme "gagner", "gratuit" ou "récompense", le modèle peut le classer comme spam.

2. Prévision des ventes  
    - **Description** : Prédire le volume de ventes futur en fonction des données historiques.
    - **Entrée** : Données passées (prix, promotions, saisonnalité).
    - **Sortie** : Montant des ventes prévu.
    - **Exemple** : En observant les ventes des mois précédents, le modèle peut prédire combien de produits seront vendus le mois prochain.

:::

:::{admonition} Algorithmes d'apprentissage supervisé

- Régression Linéaire  
    - **Utilité** : Prédire une **valeur continue** (comme le prix d’un bien immobilier).  
    - **Exemple** : Prédire le prix d’une maison en fonction de la superficie et du nombre de chambres.

- Arbres de Décision  
    - **Utilité** : Prendre des décisions basées sur plusieurs conditions.  
    - **Exemple** : Prédire si un client acceptera une offre de prêt bancaire en fonction de son âge, son salaire et son historique de crédit. L’arbre de décision divisera les données en fonction de ces critères.

- Machines à Vecteurs de Support (SVM)  
    - **Utilité** : Séparer les données en différentes classes avec une **marge maximale**.  
    - **Exemple** : Classer les patients en fonction de s’ils présentent un risque élevé ou faible pour une maladie en fonction de plusieurs paramètres (âge, pression sanguine, etc.).

:::

:::{admonition} Processus d’apprentissage supervisé  

1. **Collecte de données** : Rassembler des exemples avec leurs étiquettes (par exemple, e-mails étiquetés comme spam ou non-spam).
2. **Préparation des données** : Nettoyer et organiser les données (ex: supprimer les doublons, traiter les valeurs manquantes).
3. **Division des données** : Séparer les données en ensemble d'entraînement et ensemble de test.
4. **Entraînement du modèle** : Utiliser l’ensemble d'entraînement pour apprendre les relations entre les caractéristiques et les étiquettes.
5. **Évaluation** : Tester le modèle sur l’ensemble de test et mesurer sa performance avec des métriques comme la précision ou le taux d’erreur.
6. **Prédiction** : Utiliser le modèle entraîné pour faire des prédictions sur de nouvelles données.

:::


:::{admonition} Apprentissage Non Supervisé

L'apprentissage non supervisé est une approche de **Machine Learning** dans laquelle le modèle explore des **données non étiquetées** pour identifier des **structures cachées** ou des **modèles sous-jacents**. Contrairement à l'apprentissage supervisé, il n'y a pas de sortie ou de label prédéfini. Le but principal est de **découvrir des relations naturelles** entre les données et de les organiser en fonction de similitudes.

:::


:::{admonition} Caractéristiques de l'Apprentissage Non Supervisé  

1. **Données non étiquetées** : Le modèle ne connaît pas les réponses correctes ou les classes des données.
2. **Découverte de structures** : Cherche à trouver des groupes ou des modèles cachés.
3. **Exploration libre** : Le modèle essaie d’organiser les données sans intervention humaine.
4. **Adaptabilité** : Souvent utilisé pour analyser de nouvelles données sans connaissances préalables.

:::

:::{admonition} Applications Pratiques

1. Segmentation de la clientèle  
    - **Description** : Le modèle identifie différents groupes de clients en fonction de leurs comportements.
    - **Entrée** : Données sur les achats, la fréquence, la localisation, etc.
    - **Sortie** : Groupes (segments) de clients avec des caractéristiques communes.
    - **Exemple** : Un site e-commerce peut segmenter ses clients en "acheteurs réguliers", "acheteurs occasionnels", et "clients inactifs" pour personnaliser ses offres marketing.

2. Détection d’anomalies  
    - **Description** : L’objectif est de détecter des points de données inhabituels qui se distinguent des autres.
    - **Entrée** : Transactions bancaires d’un client.
    - **Sortie** : Transactions marquées comme normales ou suspectes.
    - **Exemple** : Une banque utilise cette technique pour identifier des fraudes potentielles, comme une transaction inhabituelle dans un pays étranger.

:::

:::{admonition} Algorithmes d'Apprentissage Non Supervisé

1. K-means (Clustering des K-means)
    - **Utilité** : Regroupe les données en **K clusters** où chaque point appartient au cluster avec le centre le plus proche.  
    - **Exemple** : Regrouper les clients d’un supermarché en fonction de leurs habitudes d'achat (par exemple, clients achetant principalement des produits biologiques vs des produits en promotion).
2. Analyse en Composantes Principales (ACP ou PCA)  
    - **Utilité** : Réduit la dimensionnalité des données tout en conservant **l'information essentielle**.  
    - **Exemple** : Simplifier un ensemble de données avec de nombreuses variables (comme les préférences des utilisateurs) pour visualiser les relations entre les clients en seulement deux dimensions.

3. Clustering Hiérarchique  
    - **Utilité** : Crée une **arborescence de clusters** où les groupes sont imbriqués. Il peut être utilisé pour analyser la structure sous-jacente d’un ensemble de données.  
    - **Exemple** : Organiser des espèces animales en fonction de leurs caractéristiques biologiques communes.

:::

:::{admonition} Processus d'Apprentissage Non Supervisé

1. **Collecte des données** : Obtenir des ensembles de données sans labels, comme les comportements des utilisateurs sur un site web.
2. **Prétraitement** : Nettoyer et normaliser les données.
3. **Application d’un algorithme** : Utiliser K-means ou ACP pour découvrir des structures.
4. **Analyse des résultats** : Examiner les clusters ou les composantes principales.
5. **Utilisation pratique** : Appliquer les insights pour prendre des décisions (ex. campagnes marketing ciblées).

:::


:::{admonition} Apprentissage par Renforcement
- **Caractéristiques** : Apprentissage à travers l’expérimentation.
- **Applications** : Jeux vidéo, robotique.
- **Composants** : Agent, environnement, récompenses.

:::

:::{admonition} Réseaux de Neurones et Apprentissage Profond
Les réseaux neuronaux reproduisent le fonctionnement du cerveau.
- **Exemples** : CNN pour les images, RNN pour les séquences.
- **Applications** : Reconnaissance faciale, génération de texte.

:::

:::{admonition} Traitement du Langage Naturel (NLP)
- **Applications** : Chatbots, traduction, résumé automatique.
- **Avancées récentes** : GPT-4, BERT/Gemini, transformers.

:::

:::{admonition} Vision par Ordinateur
- **Applications** : Voitures autonomes, surveillance, imagerie médicale.
- **Défis** : Gestion des occlusions, apprentissage avec peu de données.

:::

:::{admonition} Systèmes Experts
- **Applications** : Diagnostic médical, configuration de réseaux.
- **Avantages** : Expertise en continu.
- **Limites** : Difficulté à mettre à jour les règles.

:::

:::{admonition} Robotique
- **Applications** : Industrie, exploration spatiale, drones.
- **Défis** : Interaction homme-robot, planification de trajectoires.

:::

:::{admonition} Représentation des Connaissances
- **Applications** : Web sémantique, aide à la décision.
- **Défis** : Intégration de sources diverses, gestion de l'incomplétude.

:::


-----




## Projet d'Analyse : L'Intelligence Artificielle dans la Transformation Digitale d'une Entreprise Marocaine

### Mise en Situation

Vous êtes consultants pour "Marjane Holding", une entreprise marocaine de grande distribution souhaitant moderniser son approche commerciale en intégrant l'intelligence artificielle (IA). Face à une concurrence accrue dans le secteur de la grande distribution et à l'évolution des attentes des consommateurs, l'entreprise cherche des moyens de mieux comprendre ses clients, d'optimiser la gestion de ses stocks et de personnaliser l’expérience d’achat.

### Objectifs du Projet
1. **Assimilation des concepts clés de l'IA** : Les étudiants devront rechercher et définir les concepts d'intelligence artificielle, de machine learning, et de big data pour bien cerner leurs applications pratiques.
2. **Découverte de l'apprentissage supervisé** : Les étudiants exploreront des cas concrets d'apprentissage supervisé (classification et régression) et réfléchiront à leur utilisation dans des scénarios réels adaptés au contexte de Marjane Holding.
3. **Analyse des besoins en données** : Les étudiants examineront les sources de données, les types de données nécessaires, et la forme des données utilisées dans l'apprentissage supervisé.
4. **Développement de recommandations théoriques** : Les étudiants formuleront un plan d'action pour la modernisation de l’entreprise en utilisant l’IA.

### Partie 1 : Compréhension des Concepts Clés 

#### Concepts à Rechercher et Définir

Les étudiants devront faire des recherches pour définir et expliquer les concepts suivants :
1. **Intelligence Artificielle (IA)** 
2. **Machine Learning (ML)**
3. **Apprentissage Supervisé** 
4. **Classification et Régression** 
5. **Big Data** 
#### Questions Guidées
1. Quelles sont les principales différences entre l'IA et le machine learning ?
2. Pourquoi utilise-t-on des données étiquetées dans l'apprentissage supervisé ?
3. Quels sont les différents types de données (structurées et non structurées) et comment peuvent-ils être utilisés en apprentissage supervisé ?
4. Pourquoi le Big Data est-il important pour le développement de l'IA, en particulier dans un secteur comme la grande distribution ?

### Partie 2 : Analyse des Besoins en Données et Apprentissage Supervisé

#### Cas Pratiques à Analyser

Pour chaque défi rencontré par Marjane Holding, analysez les éléments suivants :
1. **Sources de Données** : Identifiez les sources de données potentielles.
2. **Types de Données** : Précisez si les données sont structurées ou non structurées et expliquez comment elles pourraient être utilisées en apprentissage supervisé.
3. **Format des Données** : Discutez de la forme des données (texte, images, chiffres) et de l'importance de la qualité des données pour obtenir de bons résultats.
4. **Application du Modèle** : Choisissez le type d’apprentissage supervisé adapté pour chaque défi.

##### Situation 1 : Prédiction des Ventes Futures
- *Données disponibles* : Historique des ventes, calendrier des fêtes marocaines, promotions, saisonnalité.
- *Questions* :
  - Quelles sources de données Marjane pourrait-elle utiliser pour améliorer la précision des prédictions de ventes ?
  - Quels types de données supplémentaires pourraient être utiles pour affiner les prévisions ?
  - Comment la forme des données (tableaux de ventes, graphiques de tendances) influence-t-elle le choix du modèle d’apprentissage supervisé ?

##### Situation 2 : Personnalisation du Service Client
- *Données disponibles* : Historique des interactions clients, réclamations, avis clients, FAQ existante.
- *Questions* :
  - Quelle est la nature des données client (structurées ou non structurées) et comment cela influence-t-il le type d'algorithme de classification à utiliser ?
  - Quelles données complémentaires Marjane pourrait-elle collecter pour mieux personnaliser le service client ?
  - Quels défis l’entreprise pourrait-elle rencontrer lors de l’utilisation de données textuelles (ex. : compréhension des avis clients) dans un modèle d’apprentissage supervisé ?

##### Situation 3 : Optimisation de la Gestion des Stocks
- *Données disponibles* : Historique des ventes, prévisions météo, stocks actuels, informations sur les fournisseurs.
- *Questions* :
  - Comment les données structurées (quantités de stock, historiques de ventes) et non structurées (informations sur les fournisseurs) peuvent-elles être combinées pour une meilleure gestion des stocks ?
  - Quel type d’apprentissage supervisé serait adapté pour prévoir la demande des produits en fonction de la saisonnalité ?
  - Comment Marjane pourrait-elle maintenir la qualité et la fiabilité des données pour garantir l’efficacité du modèle ?

### Partie 3 : Recommandations Théoriques 

#### Plan d'Action à Développer

Formulez un plan d’action en réponse aux questions suivantes :
1. **Identification des Besoins en Données** :
   - Quelles données Marjane doit-elle collecter ou mettre en place pour assurer le succès des projets IA (précisez les sources, types et formats de données nécessaires) ?
   - Comment Marjane pourrait-elle vérifier et maintenir la qualité des données dans le temps ?

2. **Priorité des Solutions** :
   - Classez les solutions par ordre de priorité en fonction de leur impact sur le business, leur facilité de mise en œuvre, leur coût estimé et les risques potentiels.
   
3. **Feuille de Route** :
   - Court terme (3-6 mois) : Quels petits projets IA Marjane pourrait-elle lancer pour explorer l'apprentissage supervisé ?
   - Moyen terme (6-12 mois) : Quelle application IA pourrait-elle introduire pour transformer le service client ?
   - Long terme (12+ mois) : Comment Marjane pourrait-elle devenir une entreprise orientée "data" en intégrant des solutions IA avancées ?

#### Questions Finales
1. Quelles sont les trois principales recommandations que vous feriez à Marjane pour moderniser son approche avec l'IA et le machine learning ?
2. Quels indicateurs de performance (KPIs) recommanderiez-vous pour évaluer le succès de chaque solution IA ?
3. Comment Marjane pourrait-elle promouvoir l’adoption de l’IA parmi les employés, et quels défis pourraient apparaître ?

---


