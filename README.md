<div align="center">
# 🇷🇪 CASUD Monitor

Tableau de bord expert de la Communauté d'Agglomération du Sud — La Réunion.

![HTML5](https://img.shields.io/badge/HTML-5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS-3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

![Leaflet](https://img.shields.io/badge/Leaflet-1.9.4-199900?style=flat-square&logo=leaflet&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?style=flat-square&logo=chart.js&logoColor=white)

![Modules](https://img.shields.io/badge/modules-9-purple?style=flat-square)
![Sous-onglets](https://img.shields.io/badge/sous--onglets-25-orange?style=flat-square)
![Arrêts](https://img.shields.io/badge/arrêts%20CarSud-2%20141-blue?style=flat-square)
![Opérations](https://img.shields.io/badge/opérations%20CPER-146-red?style=flat-square)
![Status](https://img.shields.io/badge/status-production-success?style=flat-square)

Dashboard interactif pour le pilotage de la **CASUD** (5 communes) : Le Tampon, Saint-Joseph, Saint-Philippe, Entre-Deux, Petite-Île.

🚀 [Voir le dashboard](https://gunout.github.io/casud-monitor/) · 📊 [data.regionreunion.com](https://data.regionreunion.com)
</div>

---

## 🎯 Présentation

**CASUD Monitor** est un tableau de bord web autonome (HTML + JS + CSS, sans backend) pour le pilotage de la Communauté d'Agglomération du Sud.

Il agrège 3 sources :

- 🏛️ casud.re — RPQS Déchets/Eau 2024, Budget, ITI (PDF)
- 🌐 data.regionreunion.com — CPER, Permis, CAF, BP Région (APIs)
- 🚌 transport.data.gouv.fr — GTFS CarSud (2 141 arrêts)

Le dashboard couvre **9 domaines métier** répartis en **25 sous-onglets**.

---

## ✨ Fonctionnalités

- 🌙 Thème sombre "cyber" avec police JetBrains Mono
- 📱 Responsive (desktop / tablette / mobile)
- 📈 Graphiques Chart.js (barres, lignes, doughnuts)
- 🗺️ Cartes Leaflet (marqueurs, clusters, polylignes)
- 📋 Tableaux interactifs (tri, scroll, tooltips)
- 🔢 KPI dynamiques en dégradé cyan
- 🚨 Module Alertes avec détection automatique
- 💾 Données JSON locales (aucun appel API pour les données CASUD)

---

## 🗂️ Modules

| Module | Icône | Contenu | Sous-onglets |
|---|:---:|---|:---:|
| Vue d'ensemble | 📊 | KPIs globaux | — |
| Alertes | 🚨 | Diagnostic automatique | 4 |
| Transport | 🚌 | GTFS CarSud + carte | 4 |
| Déchets | 🗑️ | RPQS 2024 + SINOE | 4 |
| Eau & Assainissement | 💧 | RPQS 2024 | — |
| Habitat | 🏘️ | Permis + CAF + logements | 4 |
| Énergie | ⚡ | Réseau EDF + projets | 4 |
| Finances | 💰 | BP Région 2020 | 4 |
| Investissements | 🏗️ | 146 opérations CPER | Filtres + CSV |
| À propos | ℹ️ | Documentation | — |

### Contenu détaillé

**🚌 Transport** : 2 141 arrêts, 43 lignes, 1 352 trajets, 128 tracés géographiques + carte interactive MarkerCluster.

**🏘️ Habitat** : 2 500 permis de construire, 9 253 logements créés, 654 791 m² de surface habitable, bénéficiaires CAF.

**🏗️ Investissements** : 146 opérations CPER, 151,3 M€ coût HT, 79,9 M€ subventions, filtres par commune/domaine/période, export CSV.

---

## 🚀 Installation

### En ligne (GitHub Pages)

https://gunout.github.io/casud-monitor/

### Local

    git clone https://github.com/gunout/casud-monitor.git
    cd casud-monitor
    python3 -m http.server 8060

Ouvrir : http://localhost:8060

### Déploiement

Le fichier index.html est 100% autonome. Compatible GitHub Pages, Netlify, Vercel, Cloudflare Pages.

---

## 📡 Sources de données

### 🏛️ CASUD (casud.re)

- RPQS Déchets 2024 — 34 801 t OMR, +13,78%
- RPQS Eau Potable 2024 — 133 164 habitants desservis
- RPQS ANC 2024 — 45 142 usagers
- RAD Transports 2023 — 1,13 M clients
- Budget 2024 — 20,8 M€ d'excédent

### 🌐 Région (data.regionreunion.com)

- test_tcomhs — 146 opérations CPER CASUD
- liste-des-permis-de-construire — 2 500 permis
- beneficiaires-presta-sociales-caf — Bénéficiaires CAF
- bp_012020_lareunion — 1 104 lignes budget Région
- developpement-et-lineaire-du-reseau-electrique-edf — 15 lignes

### 🚌 Transport (transport.data.gouv.fr)

- GTFS CarSud — 2 141 arrêts, 43 lignes, 1 352 trajets

---

## 🛠️ Stack technique

| Composant | Technologie |
|---|---|
| Structure | HTML5 |
| Styles | CSS3 (variables, grid, flexbox) |
| Logique | JavaScript ES6+ (async/await) |
| Graphiques | Chart.js 4.4 |
| Cartes | Leaflet 1.9.4 |
| Clustering | Leaflet.markercluster 1.5.3 |
| Polices | JetBrains Mono + Inter |
| Tuiles cartes | OpenStreetMap |

### Charte graphique

| Rôle | Code |
|---|---|
| Fond principal | #050810 |
| Cartes | #0a0f1a |
| Accent cyan | #00e5ff |
| Succès vert | #00ff88 |
| Avertissement | #ffb800 |
| Erreur rouge | #ff3b3b |
| Info violet | #a855f7 |

---

## 📁 Structure du projet

    casud-monitor/
    ├── index.html
    ├── README.md
    ├── LICENSE
    ├── .gitignore
    └── data/
        ├── casud-data.json
        ├── carsud-stops.json
        ├── carsud-routes.json
        ├── carsud-shapes.json
        └── carsud-stats.json

---

## 🤝 Contribution

    git clone https://github.com/VOTRE_USERNAME/casud-monitor.git
    cd casud-monitor
    git checkout -b feature/mon-module
    python3 -m http.server 8060
    git commit -m "feat: ajout du module XYZ"
    git push origin feature/mon-module

### Convention de commits

- feat : Nouvelle fonctionnalité
- fix : Correction de bug
- docs : Documentation
- style : Formatage
- refactor : Refactoring
- perf : Performance
- chore : Maintenance

---

## 📄 Licence

MIT — voir [LICENSE](LICENSE)

---
<div align="center">
🌴 Fait avec ❤️ à La Réunion

Sources : casud.re · data.regionreunion.com · transport.data.gouv.fr
</div>
