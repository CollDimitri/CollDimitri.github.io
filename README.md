# Portfolio BTS SIO SISR — Dimitri COLL

Portfolio en ligne réalisé dans le cadre du **BTS SIO option SISR** (Solutions d'Infrastructure, Systèmes et Réseaux) à **Nexa Digital School** (Paris 10ᵉ), session 2026. Ce site regroupe mes situations professionnelles, mon tableau de synthèse E4, ma veille technologique et mon CV.

**Alternance en cours** : Technicien support & infrastructure au sein du groupe **SNCF Voyageurs**.

🔗 **Site publié** : `https://dimitricollPortfolio.github.io`

---

## 🧭 Structure du site

```
dimitricollPortfolio.github.io/
├── index.html              · page d'accueil + hero
├── about.html              · parcours, formation, stages
├── competences.html        · blocs 1 & 2 · certifications
├── projets.html            · index des 7 projets SISR
├── projets/
│   ├── active-directory.html
│   ├── pfsense.html
│   ├── vlan-cisco.html
│   ├── supervision-zabbix.html
│   ├── glpi.html
│   ├── serveur-linux.html
│   └── sauvegarde-veeam.html
├── veille.html             · veille techno (ransomwares)
├── e4.html                 · tableau de synthèse E4
├── contact.html            · formulaire + infos
├── css/style.css           · design system complet
├── js/main.js              · interactions (menu, anims)
└── assets/
    ├── documents/CV-Dimitri-COLL.pdf
    └── images/*.svg        · schémas d'architecture
```

---

## 🚀 Publier sur GitHub Pages

### 1. Créer le dépôt

Sur GitHub, créez un nouveau dépôt **public**. Pour un site personnel à la racine, le nom doit être exactement :

```
dimitricollPortfolio.github.io
```

> Par exemple, si votre pseudo GitHub est `dimitricoll`, le dépôt doit s'appeler `dimitricoll.github.io`.

### 2. Pousser le contenu

Depuis ce dossier, en ligne de commande :

```bash
git init
git branch -M main
git add .
git commit -m "Initial commit : portfolio BTS SIO SISR"
git remote add origin https://github.com/awseyyy/dimitricollPortfolio.github.io.git
git push -u origin main
```

### 3. Activer GitHub Pages

1. Dans le repo GitHub → onglet **Settings**
2. Menu de gauche → **Pages**
3. Section *Build and deployment* → Source : **Deploy from a branch**
4. Branch : `main` / Folder : `/ (root)` → **Save**

Le site est accessible à `https://dimitricollPortfolio.github.io` au bout de 1 à 2 minutes.

---

## ✅ Informations déjà personnalisées

| Donnée | Valeur |
|---|---|
| Nom complet | Dimitri COLL |
| Âge | 19 ans |
| E-mail | contact.dimitricoll@gmail.com |
| Téléphone | 06 51 21 49 22 |
| LinkedIn | linkedin.com/in/dimitri-coll-4270853b6 |
| École | Nexa Digital School (Paris 10ᵉ) |
| Lycée d'origine | Lycée des Métiers Sully (Bac Pro SN, 2021-2024) |
| Alternance | SNCF Voyageurs (2024-2026, en cours) |
| Stages SNCF | Fibre optique (2022), Service info (2023), Service info (2024) |

## ✏️ Reste éventuellement à personnaliser

- **Pseudo GitHub** — si vous avez un compte GitHub public à afficher, cherchez `github.com/awseyyy` dans les fichiers et remplacez.
- **Photo de profil** — pour remplacer le monogramme "DC", vous pouvez insérer une vraie photo dans `cv-source.html` et dans `about.html`.

---

## 🔄 Régénérer le CV PDF après modification

Si vous modifiez le fichier `cv-source.html`, régénérez le PDF avec :

```bash
pip install playwright
playwright install chromium
python3 -c "
from playwright.sync_api import sync_playwright
import os
with sync_playwright() as p:
    b = p.chromium.launch()
    pg = b.new_page()
    pg.goto('file://' + os.path.abspath('cv-source.html'))
    pg.pdf(path='assets/documents/CV-Dimitri-COLL.pdf',
           format='A4', print_background=True,
           margin={'top':'0','bottom':'0','left':'0','right':'0'})
    b.close()
"
```

---

## 🛠 Stack technique

- **HTML5 sémantique**, **CSS3** avec variables personnalisées (design tokens)
- **Vanilla JavaScript** (pas de framework, pas de build step)
- **Google Fonts** : Bricolage Grotesque + Manrope + JetBrains Mono
- **SVG** inline pour les schémas et les icônes
- Compatible mobile (breakpoint 768px)
- Accessible : contrastes AA, landmarks ARIA, navigation clavier

Aucune dépendance externe autre que Google Fonts → temps de chargement < 1 seconde.

---

## 📄 Licence

Contenu personnel. Le code du design peut être librement réutilisé.
