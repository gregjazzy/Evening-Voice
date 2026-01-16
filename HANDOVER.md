# 📋 Handover — The Evening Voice Presentation

> Présentation web style Keynote pour cliente milliardaire

**Date** : 16 janvier 2026  
**État** : 🔄 En cours — Problème CSS à corriger

---

## 🎯 Contexte

**Client** : Top 40 fortunes mondiales (~10 milliards €)  
**Projet** : Application "The Evening Voice" pour ses 2 filles  
**Langue** : Anglais (traduit du français)  
**Déploiement** : https://evening-voice.netlify.app (auto-deploy depuis GitHub)

---

## 📁 Structure du projet

```
Voice/
├── presentation/
│   ├── index.html              ← La présentation (20 slides)
│   ├── background.png          ← Image de fond (fille + lanterne)
│   ├── 01-journal-accueil.png  ← Screenshots de l'app
│   ├── 02-ecriture-liste.png
│   ├── 03-ecriture-histoire-editeur.png
│   ├── 04-montage-selection.png
│   ├── 05-montage-editeur-complet.png
│   ├── 06-montage-effets-selection.png
│   ├── 07-studio-creation.png
│   └── 08-theatre-vide.png
├── netlify.toml                ← Config Netlify (publish: presentation/)
└── HANDOVER.md                 ← Ce fichier
```

---

## 🚀 Lancer en local

```bash
cd /Users/gregorymittelette/Dev/Voice
python3 -m http.server 3004
```

Puis ouvrir → **http://localhost:3004/presentation/index.html**

### Navigation
- **← →** Flèches clavier
- **Home** Premier slide
- **End** Dernier slide
- **Swipe** sur mobile

---

## 📊 Structure des 20 slides

| # | Slide | Contenu |
|---|-------|---------|
| 1 | **The Evening Voice** | Titre + background avec fille/lanterne |
| 2 | **The Vision** | Objectifs : prompting, autonomie, publication |
| 3 | **Six Pedagogical Objectives** | 6 cartes numérotées |
| 4 | **Luna, the AI Friend** | Présentation de Luna (avatar + traits) |
| 5 | **The Pedagogical Philosophy** | Quote + autonomie + transferable skills |
| 6 | **Luna's 3 Golden Rules** | Friend not teacher, Guide with questions, Never do it for them |
| 7 | **Luna in Action — Images** | Dialogue exemple (5 Magic Keys) |
| 8 | **Luna in Action — Writing** | Dialogue exemple (5 Magic Questions) |
| 9 | **The 5 Magic Questions** | WHO, WHAT, WHERE, WHEN, AND THEN |
| 10 | **The 5 Magic Keys** | Style, Hero, Mood, World, Magic |
| 11 | **Mentor Mode** | Electron + WebRTC, live video, shared control |
| 12 | **Invisible Progression** | Niveaux : Curious → AI Master |
| 13 | **The Creative Journey** | Journal → Writing → Studio → Editing → Theater |
| 14 | **Writing Mode** | Screenshot + features list |
| 15 | **Editing Mode** | Screenshot + features list |
| 16 | **Theater Mode** | AirPlay, Chromecast, HDMI, DLNA, Hue |
| 17 | **Smart Home Integration** | Philips Hue ambiances |
| 18 | **Three Native Languages** | English, Russian, French |
| 19 | **The Curriculum** | ⚠️ NOUVEAU — 3 disciplines + 3 pillars + Mentor Dashboard |
| 20 | **Final** | The Evening Voice — closing |

---

## ✏️ Modifications récentes (16 janvier 2026)

### Session actuelle

| Action | Détail |
|--------|--------|
| ✅ **Slide "The Curriculum" créée** | Remplace "What the Girls Learn" |
| ✅ **Vocabulaire prestigieux** | Prompt Engineering Mastery, Narrative Architecture, Visual Direction |
| ✅ **3 Pillars of Excellence** | Linguistic Precision, Cause & Effect Logic, Strategic Multilingualism |
| ✅ **Mentor Mode Dashboard** | Mention analytics de progression |
| ✅ **Layout 2 colonnes** | Disciplines à gauche, Pillars à droite (centrés) |
| 🔄 **Problème background** | Image ne couvre pas toute la largeur sur grands écrans |

### Sessions précédentes

| Action | Détail |
|--------|--------|
| ✅ **Traduction anglais** | Toute la présentation traduite |
| ✅ **"l'enfant" → "the girls"** | Adapté au contexte |
| ✅ **Slide Mentor Mode ajoutée** | Electron + WebRTC |
| ✅ **Version mobile** | Responsive iPhone Pro Max |
| ✅ **Emojis remplacés** | Icônes SVG Apple-style |
| ✅ **Déploiement Netlify** | Auto-deploy depuis GitHub |

---

## 🐛 Bug en cours

### Problème : Background qui ne couvre pas toute la largeur

**Symptôme** : Sur les slides titre et final, l'image `background.png` ne couvre pas toute la largeur de l'écran — bande grise/violette visible à droite.

**Cause probable** : L'image a une résolution fixe et le CSS `background-size: cover` ne fonctionne pas correctement sur très grands écrans.

**CSS actuel** (ligne ~147) :
```css
.title-slide {
  background: linear-gradient(...),
              url('./background.png') center center / cover no-repeat;
}
```

**Solutions possibles** :
1. Utiliser une image plus large ou générer un pattern qui se répète
2. Ajouter un fallback avec `background-color` qui match les bords de l'image
3. Forcer `min-width: 100vw` sur le slide

---

## 🎨 Design

### Palette
- **Fond** : Dégradé violet (#1a0a2e → #2d1b4e → #4a2c7a)
- **Accent** : Or (#C9A962, #E8D5A3, #8B7355)
- **Texte** : Blanc cassé (#FEFEFE)

### Typographies
- **Titres** : Playfair Display (serif élégant)
- **Corps** : Cormorant Garamond (serif classique)
- **UI** : Montserrat (sans-serif)

### Effets
- Étoiles animées (twinkle)
- Lueur de lanterne pulsante
- Animations d'entrée (fadeInUp)

---

## 🔗 Liens

- **GitHub** : https://github.com/gregjazzy/Evening-Voice
- **Netlify** : https://evening-voice.netlify.app
- **Projet principal** : `/Users/gregorymittelette/Dev/lavoixdusoir/`

---

## 📝 Pour modifier

Le fichier `presentation/index.html` contient tout (HTML + CSS + JS).

### Structure d'un slide
```html
<section class="slide content-centered stars" data-slide="X">
  <h2 class="section-header animate-in">Titre</h2>
  <p class="paragraph animate-in animate-in-delay-1">Contenu...</p>
</section>
```

### Classes importantes
- `.stars` — Étoiles animées en fond
- `.title-slide` / `.final-slide` — Slides avec background image
- `.split-slide` — Layout 2 colonnes (image + contenu)
- `.animate-in-delay-X` — Animation décalée (1, 2, 3, 4)

### Media queries
- Desktop : par défaut
- Tablette : `@media (max-width: 1200px)`
- Mobile : `@media (max-width: 480px)`

---

## ✅ Checklist avant présentation

- [ ] Bug background corrigé
- [ ] Tester sur l'écran de présentation réel
- [ ] Navigateur en plein écran (F11 / Cmd+Shift+F)
- [ ] Commencer slide 1 (touche Home)
- [ ] Tester navigation ← →

---

## 📞 Contact

Dernière modification par : **Claude (Cursor AI)**  
Date : 16 janvier 2026

---

**Bonne chance pour la suite !** 🌙✨
