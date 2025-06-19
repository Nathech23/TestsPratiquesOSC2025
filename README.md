#  Orange Client Analytics - Summer Challenge 2025

##  Candidat
**Nom :** NZIELEU NGNOULAYE  
**Prénom :** Magdiel Nathan  
**Profil :**  Data Science - Big data

---

##  Librairies utilisées

### **Manipulation et analyse des données**
- **pandas** - Chargement, nettoyage et manipulation du dataset  
- **numpy** - Calculs numériques et opérations matricielles

### **Visualisations**
- **matplotlib** - Graphiques de base et personnalisation  
- **seaborn** - Visualisations statistiques avancées et styling

### **Machine Learning**
- **scikit-learn** - Clustering et réduction de dimensionnalité  
  - `StandardScaler` - Standardisation des variables  
  - `KMeans` - Algorithme de clustering  
  - `PCA` - Analyse en composantes principales  

### **Utilitaires**
- **warnings** - Suppression des alertes non critiques

---

##  Résumé des observations

###  **Qualité des données**
- **Dataset propre** : 1000 clients, 8 variables, 0 valeur manquante  
- **Répartition équilibrée** : 5 régions du Cameroun représentées  
- **Mix forfaits** : 70.4% prépayés vs 29.6% postpayés

###  **Profil client moyen**
- **Âge** : 43.8 ans (18-69 ans)  
- **Consommation data** : 1510 Mo/mois (1.5 Go)  
- **Minutes d'appels** : Variable selon forfait  
- **Facture moyenne** : 5069 FCFA/mois

###  **Insights majeurs découverts**

####  **Anomalie tarifaire identifiée**
- **Clients postpayés** : Consomment PLUS de data (1575 Mo) mais paient MOINS (4967 FCFA)  
- **Clients prépayés** : Consomment moins de data (1482 Mo) mais paient PLUS (5112 FCFA)  
- **Impact** : Grille tarifaire à revoir pour optimiser revenus

####  **Répartition géographique**
- **Région dominante** : Adamaoua (21.2% des clients)  
- **Région sous-représentée** : Centre (17.8% seulement)  
- **Opportunité** : Renforcer présence dans certaines zones

####  **Segmentation client (4 clusters identifiés)**
1. **Cluster PREMIUM** : Forte consommation + forte facture  
2. **Cluster OPPORTUNITÉ** : Forte consommation + faible facture → **UPSELLING**  
3. **Cluster RISQUE** : Faible consommation + forte facture → **CHURN**  
4. **Cluster STANDARD** : Profil équilibré

###  **Métriques de clustering**
- **Variance PCA expliquée** : ~65% avec 2 composantes  
- **Segmentation claire** des comportements clients  
- **Clusters exploitables** pour actions marketing

---

##  Recommandations business

###  **1. Actions prioritaires par segment**

####  **Cluster OPPORTUNITÉ (Forte conso + Faible facture)**
- **Cible** : Clients consommant > moyenne data mais facture < moyenne  
- **Action** : **UPSELLING URGENT**  
- **Offre** : Migration vers forfait data illimitée (+30% revenus estimés)  
- **Canal** : SMS + Email + Appel commercial

####  **Cluster RISQUE (Faible conso + Forte facture)**
- **Cible** : Clients sous-utilisant leur forfait  
- **Action** : **RÉTENTION**  
- **Offre** : Forfait adapté à leur usage réel (-15% prix, éviter churn)  
- **Canal** : Centre d'appels avec offre personnalisée

####  **Cluster PREMIUM (Forte valeur)**
- **Action** : **FIDÉLISATION VIP**  
- **Offre** : Programme fidélité, services exclusifs, accès prioritaire  
- **Canal** : Communication premium personnalisée

###  **2. Migrations de forfait recommandées**
- **Migration prépayé → postpayé** pour gros consommateurs data  
- **Critère** : Clients prépayés avec data > moyenne globale  
- **Bénéfice** : Optimisation facture client + augmentation revenus Orange

###  **3. Offres personnalisées**
- **SMS intensifs** : Bonus SMS pour clients > 1.5x moyenne  
- **Data personnalisée** : Forfaits adaptés par région (urbain vs rural)  
- **Géolocalisation** : Offres spécifiques par région selon profil local

###  **4. Impact business estimé**
- **Potentiel d'augmentation CA** : +15-25% sur segments ciblés  
- **ROI élevé** : Clients déjà engagés, conversion facilitée  
- **Réduction churn** : -15% sur clusters à risque

---

##  Ce qui aurait pu être ajouté avec plus de temps

###  **Analyses approfondies du dataset Orange**

####  **Optimisation du clustering**
- **Méthode du coude** : Déterminer scientifiquement le nombre optimal de clusters (au lieu de k=4 fixe)  
- **DBSCAN** : Comparer avec KMeans pour détecter des clusters de densité  
- **Score de silhouette** : Évaluer quantitativement la qualité de la segmentation  

####  **Analyses comportementales spécifiques**
- **Profils de consommation détaillés** : Ratios data/appels/SMS par âge et région  
- **Analyse des outliers** : Identifier les clients aux comportements extrêmes  
- **Segmentation par âge** : Profils générationnels (18-30, 31-45, 46-60, 60+)  
- **Patterns régionaux** : Comportements spécifiques urbain (Centre/Littoral) vs rural

####  **Analyses tarifaires poussées**
- **Rentabilité par client** : Calculer le coût vs revenus par profil  
- **Élasticité prix** : Analyser l'impact des variations tarifaires sur la consommation  
- **Cross-selling** : Identifier les combinaisons gagnantes data+appels+SMS  
- **Pricing optimal** : Recommander des grilles tarifaires par cluster

###  **Analyses géographiques spécifiques Cameroun**

####  **Deep dive par région**
- **Centre & Littoral** : Profils urbains vs opportunités data/digital  
- **Adamaoua, Nord-Ouest, Sud-Ouest** : Stratégies rurales adaptées  
- **Migration interne** : Analyser les mouvements entre régions  
- **Pénétration Orange** : Comparer la part de marché par zone


###  **Modélisation prédictive avec nos données**

####  **Prédiction churn**
- **Features engineering** : Créer des indicateurs de risque (ratio facture/usage)  
- **Modèle binaire** : Prédire la probabilité de résiliation  
- **Early warning** : Alertes sur clients à risque dans chaque cluster


### **Visualisations avancées spécifiques**

####  **Cartographie Cameroun**
- **Carte choroplèthe** : Densité clients et revenus par région  
- **Heatmap consommation** : Visualisation géographique des usages  
- **Comparaison régionale** : Benchmarks visuels entre zones

####  **Dashboards interactifs**
- **Filtres dynamiques** : Par âge, région, forfait, cluster  
- **Drill-down** : Navigation de la vue globale au client individuel  
- **Simulateurs** : Impact des changements tarifaires en temps réel

###  **Analyses de corrélations avancées**

####  **Relations cachées**
- **Âge vs technologie** : Adoption data selon générations  
- **Géographie vs comportement** : Impact région sur mix consommation  
- **Forfait vs satisfaction** : Adéquation offre/usage par segment  
- **Saisonnalité simulée** : Extrapoler les variations mensuelles



---

##  Conclusion

Cette analyse révèle des **opportunités business concrètes** chez Orange Cameroun :
- **Segments clients clairement identifiés** avec actions ciblées  
- **Anomalies tarifaires** à corriger pour optimiser revenus  
- **Potentiel d'upselling** significatif sur clients sous-facturés  
- **Stratégies de rétention** pour réduire le churn

---

**Projet réalisé dans le cadre de l'Orange Summer Challenge 2025**  
**Durée** : 4 heures | **Technologies** : Python, Google Colab, Scikit-learn  
