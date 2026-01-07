
# Analyse de l’impact des incitations sur la croissance du revenu d’une plateforme de VTC
Scroll down for an English version of this READ ME

## Contexte

Ce projet a pour but d’évaluer **l’impact des incitations marketing et professionelles** (remise de bienvenue, points et prime objectif) sur le **revenu d’une plateforme de VTC fictive**.

Afin d’arriver à des conclusions pertinentes, j’ai basé mes comparaisons sur quatre indicateurs clés :
- le **revenu moyen**,
- le **revenu médian**,
- le **revenu total**,
- le **nombre de trajets effectués**.

Le **revenu médian net** a été utilisé comme indicateur principal, car il reflète mieux la valeur « typique » d’une course, sans être influencé par des valeurs extrêmes ou outliers.

Concrètement, ma compagnie fictive de VTC cherche à répondre aux questions suivantes :
- **Quelle incitation rapporte le plus de revenu ?**
- **Quand faut-il activer les incitations ?**
- **Où faut-il les activer ?**
- **Sur quels clients et quels chauffeurs faut-il les cibler ?**

Un meilleur ciblage permettrait à l’entreprise de **mieux allouer ses ressources** et d’atteindre une **croissance plus rentable**.  J’ai donc analysé, en complément des incitations, des paramètres tels que :
- la **situation géographique**,
- les **segments de clients et de chauffeurs** (par fréquence d’utilisation et performance),
- les **périodes de pointe**.

---

## Approche analytique

J’ai adopté une **analyse exploratoire progressive**, basée sur des **segmentations, des filtrages et des éliminations successives**.

Mon analyse répond à une série de questions, des plus générales aux plus spécifiques.  
À chaque étape :
1. j’analyse les résultats,
2. je conserve uniquement les valeurs pertinentes,
3. je filtre le jeu de données,
4. puis je passe à la question suivante.

Cette approche m’a permis d’identifier progressivement **la combinaison de facteurs la plus rentable** pour l’entreprise.

---

## Insights clés

La combinaison générant le plus de revenu est :

**points Gowin + clients actifs + paiement par portefeuille + week-end / heures de pointe + chauffeurs performants + zones de départ les plus rentables**

---

## Méthodologie et résultats

### Q1 – Quelle incitation rapporte le plus de revenu net à l’entreprise ?

L’incitation qui rapporte le plus à l’entreprise est **le point Gowin**.

Les points Gowin sont **peu coûteux à implémenter** (environ **24 FCFA** par course) tout en générant le **meilleur revenu médian** (environ **1 150 FCFA**).  
À titre de comparaison, la **prime objectif** coûte **environ 300 FCFA**, soit **plus de 12 fois le coût des points Gowin**, tout en générant un revenu inférieur.

![Revenu médian vs coût moyen par type d'incitation](Images/Revenu_médian_vs_cout_moyen_par_type_d'incitation.png)

---

### Q2 – Les points Gowin sont-ils plus actifs sur certains segments de clients ?

Oui.  
Les points Gowin sont plus efficaces sur les segments de **nouveaux utilisateurs** et **d’utilisateurs réguliers**, que j’ai regroupés sous l’appellation **clients actifs**.

---

### Q3 – Les points Gowin sont-ils plus rentables avec un certain moyen de paiement ?

Oui.  
Le **paiement par portefeuille** s’est avéré être le **plus rentable** lorsqu’il est associé à l’incitation **points Gowin**, devant le paiement en espèces et par carte.

![Revenu médian par moyen de paiement](Images/revenu_médian_par_moyen_de_paiement.png)

---

### Q4 – Quelles sont les zones de départ les plus rentables lorsque les points Gowin sont utilisés ?

Les zones de départ les plus rentables identifiées sont :
**Gbodjè, Calavi Kpota, Cadjèhoun, Agla, Akpakpa et Fidjrossè**.

Ces zones semblent concentrer une demande suffisante et des prix de départ plus élevée par course.

![Revenu médian par zone de départ](Images/Top_5_des_zones_de_départ_les_plus_rentables.png)

---

### Q5 – Les points Gowin sont-ils plus rentables le week-end et aux heures de pointe ?

Oui.  
Les courses effectuées **le week-end** et **aux heures de pointe** génèrent un revenu médian nettement supérieur, ce qui montre que l’impact des incitations est **amplifié lors des périodes de forte demande**.

---

### Q6 – Les points Gowin sont-ils plus efficaces avec certains segments de chauffeurs ?

Oui.  
Les points Gowin sont plus rentables lorsque les courses sont attribuées à des **chauffeurs performants**.

Les chauffeurs performants affichent :
- un **revenu médian élevé** (≈ **1 330 FCFA**),
- un **volume de trajets maîtrisé** (26 trajets).

À titre de comparaison, les chauffeurs intermédiaires ont un revenu médian plus faible (**1 008 FCFA**) malgré un volume beaucoup plus élevé (146 trajets).

Cela montre que les chauffeurs performants offrent le **meilleur compromis entre rentabilité et capacité opérationnelle**.

![Revenu médian et volume par segment chauffeur](Images/revenu_médian_vs_volume_par_segment_chauffeur.png)

---

## Outils utilisés

- **Python**
- **pandas** – manipulation et analyse des données  
- **matplotlib & seaborn** – visualisation des résultats  
- **Jupyter Notebook**
- Données simulées (plateforme de VTC fictive)

---

## Ce que j’ai appris

Ce projet m’a permis de renforcer plusieurs compétences clés en analyse de données appliquée à des problématiques business réelles :

- J’ai appris à **évaluer l’impact économique des incitations**, en allant au-delà du simple volume de trajets pour raisonner en termes de **rentabilité par course**.
- J’ai compris l’importance du **choix des indicateurs**, notamment l’utilisation du **revenu médian** pour éviter des conclusions biaisées par des valeurs extrêmes.
- J’ai utilisé le principe de la **segmentation** (clients, chauffeurs, zones, périodes)
- J’ai appris à **contextualiser les résultats** en combinant rentabilité et volume, afin d’éviter des interprétations trompeuses.

Ce travail m’a surtout appris qu’une bonne analyse ne consiste pas seulement à produire des chiffres, mais à **poser les bonnes questions et à transformer les résultats en recommandations concrètes**.

--- 

## Conclusion

Cette analyse montre que **les incitations ont un impact direct et mesurable sur la croissance du revenu**, mais que leur efficacité dépend fortement du **contexte d’activation**.

Les **points Gowin** apparaissent comme le levier le plus performant, en particulier lorsqu’ils sont :
- ciblés sur des **clients actifs**,
- associés au **paiement par portefeuille**,
- activés **le week-end et aux heures de pointe**,
- combinés à des **chauffeurs performants**,
- et concentrés sur des **zones de départ à forte valeur**.

Ces résultats suggèrent qu’une stratégie d’incitation efficace ne repose pas uniquement sur le choix du mécanisme, mais sur un **ciblage précis et intelligent**, orienté vers une **croissance durable et rentable**.


---

# **Analysis of the Impact of Incentives on Revenue Growth for a Ride-Hailing Platform**

---

## **Context**

The objective of this project is to evaluate the **impact of marketing and operational incentives** (**welcome discounts, loyalty points, and performance bonuses**) on the **revenue of a fictional ride-hailing platform**.

To reach meaningful conclusions, the analysis is based on **four key performance indicators**:

* **Average revenue**
* **Median revenue**
* **Total revenue**
* **Number of completed trips**

The **net median revenue** was used as the **primary indicator**, as it better reflects the *typical* ride value and is not influenced by extreme values or outliers.

Concretely, the fictional ride-hailing company seeks to answer the following questions:

* **Which incentive generates the most revenue?**
* **When should incentives be activated?**
* **Where should incentives be activated?**
* **Which customers and drivers should be targeted?**

Better targeting would allow the company to **allocate resources more efficiently** and achieve **more profitable growth**.
To support this, the analysis also considers:

* **Geographic location**
* **Customer and driver segments** (based on usage frequency and performance)
* **Peak demand periods**

---

## **Analytical Approach**

A **progressive exploratory analysis** was conducted, based on **segmentation, filtering, and successive elimination**.

The analysis follows a sequence of questions, moving from **general insights to more specific ones**.
At each step:

1. Results are analyzed
2. Only relevant values are retained
3. The dataset is filtered
4. The analysis proceeds to the next question

This approach made it possible to progressively identify **the most profitable combination of factors** for the company.

---

## **Key Insights**

The combination that generates the **highest revenue** is:

**Gowin points + active customers + wallet payment + weekend / peak hours + high-performing drivers + most profitable pickup zones**

---

## **Methodology and Results**

### **Q1 – Which incentive generates the highest net revenue for the company?**

The incentive that generates the highest revenue is **Gowin points**.

Gowin points are **low-cost to implement** (approximately **24 FCFA per ride**) while generating the **highest median revenue** (around **1,150 FCFA**).

By comparison, the **performance bonus** costs approximately **300 FCFA**, which is **more than 12 times the cost of Gowin points**, while generating lower revenue.

![Median revenue vs average cost per incentive type](Images/Revenu_médian_vs_cout_moyen_par_type_d'incitation.png)

---

### **Q2 – Are Gowin points more effective for specific customer segments?**

Yes.
Gowin points are more effective for **new users** and **regular users**, which were grouped under the category of **active customers**.

---

### **Q3 – Are Gowin points more profitable with a specific payment method?**

Yes.
**Wallet payments** proved to be the **most profitable** when combined with **Gowin points**, outperforming **cash** and **card** payments.

![Median revenue by payment method](Images/revenu_médian_par_moyen_de_paiement.png)

---

### **Q4 – Which pickup zones are the most profitable when Gowin points are applied?**

The most profitable pickup zones identified are:

**Gbodjè, Calavi Kpota, Cadjèhoun, Agla, Akpakpa, and Fidjrossè**

These areas appear to combine **sufficient demand** with **higher base fares per ride**.

![Median revenue by pickup zone](Images/Top_5_des_zones_de_départ_les_plus_rentables.png)

---

### **Q5 – Are Gowin points more profitable during weekends and peak hours?**

Yes.
Rides completed **during weekends** and **peak hours** generate **significantly higher median revenue**, indicating that incentive impact is **amplified during periods of high demand**.

---

### **Q6 – Are Gowin points more effective with specific driver segments?**

Yes.
Gowin points are more profitable when rides are assigned to **high-performing drivers**.

High-performing drivers show:

* **High median revenue** (≈ **1,330 FCFA**)
* **Controlled trip volume** (26 trips)

By comparison, intermediate drivers generate a **lower median revenue** (**1,008 FCFA**) despite a **much higher trip volume** (146 trips).

This demonstrates that high-performing drivers offer the **best balance between profitability and operational capacity**.

![Median revenue and volume by driver segment](Images/revenu_médian_vs_volume_par_segment_chauffeur.png)

---

## **Tools Used**

* **Python**
* **pandas** – data manipulation and analysis
* **matplotlib & seaborn** – data visualization
* **Jupyter Notebook**
* **Simulated data** (fictional ride-hailing platform)

---

## **Key Learnings**

This project strengthened several core skills in **business-oriented data analysis**:

* Evaluating the **economic impact of incentives**, beyond trip volume to focus on **profitability per ride**
* Understanding the importance of **metric selection**, especially the use of **median revenue** to avoid biased conclusions
* Applying **segmentation techniques** (customers, drivers, zones, time periods)
* **Contextualizing results** by combining profitability and volume to avoid misleading interpretations

Above all, this project reinforced that good analysis is not just about producing numbers, but about **asking the right questions and turning results into actionable recommendations**.

---

## **Conclusion**

This analysis shows that **incentives have a direct and measurable impact on revenue growth**, but their effectiveness strongly depends on the **context in which they are activated**.

