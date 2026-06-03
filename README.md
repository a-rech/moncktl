# 🍸 MonCocktail

> **Votre bar à la maison** — 130 recettes de cocktails classiques et créatifs, avec la possibilité de créer, adapter et partager vos propres recettes. Accessible partout, même hors ligne.

🔗 **[Ouvrir l'application](https://a-rech.github.io/moncktl/)**

---

## ✨ Fonctionnalités principales

### 🔍 Découverte et recherche
- **Recherche par ingrédients** — sélectionnez vos ingrédients préférés, l'app trouve des cocktails possibles
- **Catalogue complet** — 130 recettes filtrables par type (Shortdrinks, Longdrinks, Tiki, etc.) ou alcool de base (Rhum, Vodka, Gin, Whisky, etc.)
- **Cocktail aléatoire** — laissez le hasard remplir votre verre
- **Profil gustatif** — barres de sucrosité, amertume et degré d'alcool sur chaque recette pour mieux choisir

### 👤 Personnalisation
- **Créer vos cocktails** — inventez vos propres recettes de zéro
- **Adapter des recettes existantes** — clonez une recette du catalogue et modifiez-la à votre goût
- **Profil gustatif personnel** — définissez vos préférences pour chaque création (sucrosité, amertume, alcool)
- **Notes personnelles** — ajoutez vos astuces, variantes ou conseils sur chaque fiche

### ❤️ Sauvegarde et évaluation
- **Favoris** — marquez vos cocktails préférés avec un ❤️ (sauvegardés automatiquement)
- **Notation** — notez chaque recette de 1 à 5 étoiles ⭐
- **Mes cocktails** — onglet dédié pour retrouver toutes vos créations et adaptations
- **Tous vos favoris retrouvés** — même après fermeture de l'app, vos données persistent

### 🔗 Partage et collaboration
- **Partager une recette** — partagez le texte lisible de la recette par SMS, Mail, WhatsApp, etc.
- **Code d'import** — générez un code unique pour partager vos créations avec d'autres utilisateurs
- **Importer des recettes** — collez un code d'import pour ajouter une recette reçue d'un ami
- **Récupération complète** — les notes et évaluations sont restaurées lors de l'import

### 💡 Ressources
- **Lexique complet** — techniques de bar, alcools, spiritueux et matériel expliqués en détail
- **Variantes suggérées** — l'app vous aide à adapter les recettes à vos ingrédients disponibles

### 📱 Accessibilité
- **PWA (Progressive Web App)** — installable sur mobile comme une vraie app
- **Fonctionne hors ligne** — Service Worker met en cache les données pour un accès sans internet
- **Mobile & Desktop** — interface responsive optimisée pour tous les écrans
- **Thème clair/sombre** — adaptez l'apparence à votre préférence
- **Navigation fluide** — 4 boutons d'accès rapide en bas (🍸 Ingrédients, 📖 Catalogue, 🎲 Hasard, ✨ Créer)

---

## 📖 Guide utilisateur

### 🏠 Page d'accueil
```
┌─────────────────────────────────────────┐
│  Shakers à la main, votre bar chez vous │
└─────────────────────────────────────────┘

[🍸 Par ingrédients]  [📖 Catalogue]  [🎲 Aléatoire]

[✨ Créer]  ← Lancer la création d'une nouvelle recette

[⚙️ Préférences]  ← Thème, données, installation...
```

### ✨ Créer une recette
```
Clique [✨ Créer]
        ↓
Choix du point de départ :
├─ [✨ Créer de zéro]        → Nouveau cocktail vierge
├─ [🍸 Adapter une recette]   → Clone une recette du catalogue
└─ [📥 Importer une recette]  → Colle un code reçu
```

### 🔗 Partager une recette
```
Ouvre une fiche recette → [🔗 Partager cette recette]
        ↓
Modal avec 2 sections :
├─ TEXTE À PARTAGER
│  ├─ [📋 Copier] → dans le presse-papiers
│  └─ [📋 Partager] → SMS, Mail, WhatsApp, etc. (si Web Share API)
│
└─ CODE D'IMPORT
   ├─ [🔐 Copier] → dans le presse-papiers
   └─ [🔐 Partager] → partage le code (si Web Share API)
```

### 📥 Importer une recette
```
Clique [✨ Créer] → [📥 Importer une recette]
        ↓
Colle le code reçu (commence par mc_recipe_v1:...)
        ↓
[✓ Importer] → Recette ajoutée avec notes et évaluations
```

---

## 🏗️ Structure du projet

```
moncktl/
├── index.html      ← Application complète (HTML/CSS/JS + 130 recettes)
├── manifest.json   ← Configuration PWA (nom, icônes, thème)
├── sw.js           ← Service Worker (cache hors ligne)
├── icon-192.png    ← Icône 192×192 (Android / Chrome)
├── icon-512.png    ← Icône 512×512 (splash screen)
└── README.md       ← Ce fichier
```

**Note** : Tout est contenu dans `index.html` (> 3900 lignes). Aucune dépendance externe.

---

## 🛠️ Technologies

- **HTML / CSS / JavaScript vanilla** — aucune dépendance (jQuery, React, Vue, etc.)
- **PWA (Progressive Web App)** — Service Worker + Web App Manifest
- **localStorage** — persistance des favoris, notes, évaluations, créations
- **Web Share API** — partage natif sur mobile (SMS, Mail, WhatsApp, etc.)
- **Base64 UTF-8** — encodage des codes d'import avec support des emojis et accents
- **Thème dynamique** — variables CSS pour les thèmes clair/sombre
- **Google Fonts** — Playfair Display (titres) + DM Sans (corps)

---

## 📱 Installation sur mobile

### Android (Chrome, Edge, Firefox)
1. Ouvrez [https://a-rech.github.io/moncktl/](https://a-rech.github.io/moncktl/)
2. Appuyez sur le menu **⋮** (en haut à droite)
3. Sélectionnez **"Ajouter à l'écran d'accueil"**
4. Confirmez → icône 🍸 apparaît sur votre écran d'accueil
5. Lancez l'app → fonctionne hors ligne !

### iPhone / iPad (Safari)
1. Ouvrez [https://a-rech.github.io/moncktl/](https://a-rech.github.io/moncktl/) dans **Safari**
2. Appuyez sur le bouton **Partager** ↑ (en bas)
3. Sélectionnez **"Sur l'écran d'accueil"**
4. Confirmez → icône 🍸 apparaît
5. Lancez l'app depuis l'écran d'accueil

---

## 🍹 Catégories et filtres

**Par alcool de base** : Rhum · Vodka · Gin · Whisky · Tequila & Mezcal · Cognac & Brandy · Champagne & Vins · Amaretto · Apéritifs

**Par type** : Shortdrinks · Longdrinks · Tiki

**Filtres avancés** : Favoris ❤️ · Mes cocktails ✦ (créations et adaptations)

---

## 🎯 Cas d'usage

### Cas 1 : Trouver un cocktail avec vos ingrédients
```
1. [🍸 Ingrédients]
2. Cochez : Rhum blanc, Menthe, Citron, Sucre
3. → L'app trouve le Mojito et autres possibilités
4. Clique sur une recette pour voir les détails
5. [❤️] pour ajouter aux favoris
```

### Cas 2 : Créer votre propre cocktail
```
1. [✨ Créer] → [✨ Créer de zéro]
2. Remplissez : titre, ingrédients, étapes
3. Réglez le profil gustatif (sliders)
4. [💾 Sauvegarder]
5. Recette disponible dans [✦ Mes cocktails]
```

### Cas 3 : Adapter une recette existante
```
1. Ouvre le Mojito
2. [✨ Adapter ce cocktail]
3. Modifiez : ajoutez plus de rhum, moins de sucre, etc.
4. [💾 Sauvegarder]
5. Votre version saved dans [✦ Mes cocktails]
```

### Cas 4 : Partager une recette créée
```
1. Ouvre votre cocktail créé
2. [🔗 Partager cette recette]
3. [📋 Copier] → texte lisible en clipboard
4. Collez dans SMS/Mail/WhatsApp
5. Ami reçoit le format texte (beau et lisible)

OU

1. [🔐 Partager] le code
2. Ami : [✨ Créer] → [📥 Importer]
3. Colle le code
4. Recette importée avec notes et étoiles !
```

---

## 🌓 Thèmes

### Thème clair (défaut)
- Fond blanc, texte noir
- Cartes avec fond gris clair
- Accents dorés

### Thème sombre
- Fond noir, texte blanc
- Cartes avec fond gris foncé
- Accents dorés (contraste optimal)
- **Textareas de partage et import** : fond blanc pour lisibilité maximale

### Changement de thème
```
[⚙️ Préférences] → Onglet "Affichage" → Toggle "Mode sombre"
```

---

## 🔐 Données et confidentialité

- **Toutes les données sont locales** — aucun serveur, aucun suivi
- **localStorage** — favoris, notes, évaluations, créations sauvegardés localement
- **Aucune connexion** — fonctionne complètement hors ligne
- **Suppression facile** — [⚙️ Préférences] → "Réinitialiser les données"

---

## 💡 Conseils de mixologie

- 🍋 **Jus frais** : toujours du jus frais citron/citron vert, pas du concentré
- 🧊 **Glaçons** : qualité premium, moins ils fondent, mieux c'est
- 🍯 **Sirop** : sucre + eau 1:1 pour un sucre liquide maison
- 🥃 **Verre** : refroidissez le verre quelques minutes avant
- 🚀 **Shaker** : secouez 10-12 secondes pour un bon mélange
- 📏 **Dose** : respectez les proportions pour un équilibre gustatif

---

## 🎨 Profil gustatif expliqué

Chaque recette (et vos créations) dispose de 3 curseurs :

```
🍬 SUCROSITÉ (0-10)
   0 = très sec (dry martini)
   5 = équilibré (mojito)
   10 = très sucré (mai tai)

🌿 AMERTUME (0-10)
   0 = très doux
   5 = équilibré
   10 = très amer (negroni)

🔥 ALCOOL (0-10)
   0 = très light (apéritif)
   5 = équilibré
   10 = très alcoolisé (shooter)
```

Utilisez ces curseurs pour trouver rapidement le cocktail idéal selon votre humeur !

---

## 🐛 Problèmes et solutions

### L'app ne fonctionne pas hors ligne
→ Vérifiez que le Service Worker est installé : [⚙️ Préférences] → "Installation"

### Mes données ont disparu
→ Elles sont stockées localement. Vérifiez que vous utilisez le même navigateur/app

### Je n'arrive pas à partager sur mobile
→ Si votre navigateur est très ancien, utilisez [📋 Copier] à la place

### Un code d'import ne marche pas
→ Assurez-vous qu'il commence par `mc_recipe_v1:` et qu'il n'est pas coupé

---

## 🚀 Roadmap future

- 🎨 Plus de thèmes (bleu, violet, rose)
- 📊 Statistiques (cocktails créés, favoris, etc.)
- 🌐 Export/Import en JSON ou PDF
- 🔄 Sync cloud optionnelle
- 👥 Partage de collections publiques
- 🎙️ Historique des cocktails testés

---

## 👨‍💻 Développement

**Technos** : HTML5 · CSS3 · JavaScript ES5+

**Build** : Aucune dépendance, aucun build tool requis

**Format** : Single-file PWA (index.html)

**Validation JS** : `node --check index.html` (JavaScript vanilla, pas de linter)

---

## 📄 Licence

Libre d'utilisation et de modification.

---

## 🍸 Crédits

Fait avec 🍸 passion pour les amateurs de mixologie.

**130 recettes classiques** compilées de sources variées (IBA, bartenders renommés).

**Merci à tous les testeurs** qui ont contribué à améliorer l'UX !

---

## 📞 Support

Avez-vous une question, une suggestion ou avez-vous trouvé un bug ?

- 🐞 **Bug** : l'app crash, un cocktail manque des données, etc.
- 💡 **Suggestion** : ajoutez une recette, modifiez un style, etc.
- ❓ **Question** : comment faire X, Y, Z ?

Ouvrez une issue ou contactez directement !

---

**Version** : 3.4  
**Dernière mise à jour** : Mai 2026  
**Status** : ✅ Production-ready

🍹 **À votre santé !**
