# 🌍 TERRA-ORBIT TOGO

**Plateforme d'observation spatiale et de simulation de résilience agro-climatique pour les petits exploitants d'Afrique de l'Ouest.**

> Développé dans le cadre du **NASA Space Apps Challenge 2026**  
> **Défi officiel :** *Field Shift: Adapting Farms with NASA Data*  
> **Zone pilote :** Togo (392 cantons couverts)

---

## 🎯 Vision & Problématique

En Afrique de l'Ouest, les petits exploitants subissent de plein fouet le dérèglement pluviométrique : faux départs de saisons, sécheresses intra-saisonnières et épuisement des sols par monoculture continue. 

**Terra-Orbit** relie les télescopes et constellations satellitaires de la NASA (**NASA POWER**, **SMAP**, **ECOSTRESS**) au terrain agricole africain pour :
1. **Évaluer l'humidité des sols et le stress hydrique** sans exiger de capteurs IoT coûteux.
2. **Simuler des successions culturales intelligentes (rotations sur 3 saisons)** qui restaurent l'azote organique, maximisent l'efficience de l'eau (WUE en FCFA/mm) et augmentent le revenu net des producteurs.
3. **Connecter la science au financement agricole** via un score de résilience climatique compréhensible par les banques (MIFA, institutions de microfinance) et les systèmes d'assurance indicielle.
4. **Garantir l'inclusion rurale** sans barrière numérique (conseils audio et alertes 2G en langues locales : Français, Éwé, Kabyè).

---

## 📊 Présentation Officielle & Pitch Deck

* 🖥️ **Deck Interactif HTML (Plein écran, Chrono 3 min & Notes jury)** :  
  [presentation-deck.html](presentation-deck.html)
* 📄 **Document Officiel PDF (Format 16:9 widescreen)** :  
  [presentation-deck.pdf](presentation-deck.pdf)

---

## 💻 Simulateur Web Interactif (`web/`)

L'application web Next.js / TypeScript permet d'explorer en direct les 392 cantons du Togo, de modéliser les successions culturales et d'adapter les prix locaux du marché.

### Lancement Rapide :
```bash
cd web
npm install
npm run typecheck
npm test
npm run dev
```
Ouvrez ensuite [http://localhost:3000](http://localhost:3000) dans votre navigateur.

---

## 🔬 Livres Blancs & Dossier Scientifique (`docs/`)

* 📑 [Dossier de soumission officiel NASA Space Apps](docs/NASA_SPACE_APPS_OFFICIAL_SUBMISSION.md)
* 🌾 [Livre blanc agronomique : Équation FAO-33, bilans hydriques et azote](docs/AGRONOMIC_ENGINE_WHITE_PAPER.md)
* 🛰️ [Downscaling satellitaire : SMAP micro-ondes (9–36 km) & ECOSTRESS thermique (70 m)](docs/REMOTE_SENSING_DOWNSCALING_WHITE_PAPER.md)
* 💳 [Modèle d'inclusion financière agricole & micro-assurance](docs/FINTECH_BUSINESS_MODEL_MIFA.md)
* ⏱️ [Script officiel du Pitch (3 minutes)](docs/PITCH_DECK_3MIN.md)
* 📋 [Contrats d'acquisition des données environnementales](docs/ENVIRONMENT_CONTRACT.md)

---

## 📂 Architecture du Projet

```text
├── docs/                     # Livres blancs, soumission NASA, modèles scientifiques
├── fintech/                  # Scoring de risque de crédit et assurance indicielle
├── pipeline/                 # Connecteurs API NASA POWER, Earthdata et régions du Togo
├── simulation/               # Modèles de cultures et moteur de rotation (FAO-33)
├── tests/                    # Suites de tests automatisés (Python & TypeScript)
├── web/                      # Interface web interactive Next.js 15 / React / Tailwind
├── app.py                    # Démonstrateur Python / Streamlit alternatif
├── presentation-deck.html    # Support de pitch interactif (jury)
├── presentation-deck.pdf     # Support de pitch PDF officiel (16:9)
└── README.md
```

---

## 🧪 Tests & Vérifications

### Tests Web & TypeScript (16 tests automatisés) :
```bash
cd web
npm test
npm run typecheck
```

### Tests Python :
```bash
python -B -m unittest tests.test_simulation_disclosure -v
```

---

## ⚖️ Licence & Transparence

Projet sous licence [MIT](LICENSE).  
*Les résultats présentés par le prototype sont exploratoires et constituent des aides à la décision destinées à être calibrées avec les données agronomiques de terrain (ITRA / ICAT).*
