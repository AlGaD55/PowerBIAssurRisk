# 📊 AssurRisk — Analyse de Sinistralité & Impact Météorologique (Power BI)

![Vue globale du tableau de bord](./assets/Vue%20globale.png)

## 🎯 Contexte & Objectifs du Projet
Afin d'optimiser sa gestion opérationnelle et financière, la direction d'**AssurRisk** a souhaité intégrer la dimension météorologique au cœur de ses analyses de sinistralité sur l'ensemble du territoire français.

* **Périmètre d'étude :** 12 098 sinistres sur 2 ans (1ᵉʳ janvier 2024 – 31 décembre 2025).
* **Enjeu financier :** 82,22 M€ de montant total estimé.
* **Objectif :** Affiner les capacités de prévision et mesurer l'impact direct des conditions climatiques (précipitations, vent, neige, codes WMO) sur la fréquence et la gravité des sinistres.
* **Note de synthèse complète :** Consultable dans le dossier `docs/` via [`Synthese AssuRisk.pdf`](./docs/Synthese%20AssuRisk.pdf).

---

## 🛠️ Stack Technique & Modélisation
* **Préparation & Modélisation :** Modèle en étoile, mesures DAX dynamiques (coût moyen prévisionnel, taux d'indemnisation réel, ratios fréquence / gravité).
* **Data Visualisation :** Power BI Desktop (rapports disponibles dans le dossier `reports/`).

---

## 📈 Aperçu du Tableau de Bord & Analyses Clés

### 1. Vue Globale, Santé Financière & KPI
![Vue globale](./assets/Vue%20globale.png)

* **Taux d'indemnisation réel (67,02 %) :** Environ deux tiers des dossiers font l'objet d'un règlement financier effectif (avec 4 800 dossiers clôturés et 1 800 dossiers refusés). Le montant total indemnisé reste inférieur au montant total estimé, témoignant d'une gestion budgétaire maîtrisée.
* **Répartition géographique :** **5 régions** concentrent à elles seules **plus de 60 % des sinistres** (7 422 dossiers), pour un montant estimé de **51,17 M€** (et **33,87 M€** d'indemnisation effective), principalement lié à un effet de volume démographique et de biens assurés.
* **Paradoxe du volume météo :** Le volume brut de sinistres est plus élevé par temps calme en raison de la plus grande fréquence des journées sans intempéries sur l'année.

### 2. Typologie des Sinistres & Sévérité Météorologique
![Typologie des sinistres](./assets/Typologie%20sinistre.png)

* **Gravité vs Fréquence (Coût moyen basé sur le montant estimé) :**
  * **Forte sévérité unitaire :** *Incendie* (**27 548,10 €** / sinistre) et *Inondation* (**18 111,01 €** / sinistre) représentent les risques les plus sévères financièrement.
  * **Forte fréquence :** *Dégâts des eaux* et *Bris de glace* concentrent la majorité du volume global avec un coût unitaire plus modéré.
* **Impact des épisodes dégradés & codes WMO :** Lors d'événements météorologiques marqués (tempêtes, inondations sévères), le coût moyen par sinistre augmente fortement. Les codes WMO mettent en évidence un lien direct entre ciel couvert avec pluies modérées et hausse des déclarations de *dégâts des eaux* et de *tempêtes*.

---

## 💡 Recommandations Stratégiques
1. **Dispositifs de prévention ciblés :** Mettre en place un système d'alerte automatisé (SMS / notifications) lors de bulletins météo défavorables (vent fort, grêle) afin de réduire les bris de glace et sinistres évitables.
2. **Allocation prioritaire des fonds de réserve :** Orienter en priorité les réserves de capital vers les 5 régions présentant la plus forte exposition financière.

---

## 📂 Structure du Dépôt
```text
BRIEF POWER BI FINAL/
├── assets/
│   ├── Typologie sinistre.png
│   └── Vue globale.png
├── docs/
│   └── Synthese AssuRisk.pdf
├── reports/                 # Fichiers de rapport Power BI (.pbix / exports)
└── README.md                # Présentation et synthèse analytique du projet