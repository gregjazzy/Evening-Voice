# 📋 Handover - Présentation Client "La Voix du Soir"

> Présentation web style Keynote pour la cliente multi-milliardaire

**Date** : 15 janvier 2026  
**État** : ✅ Prête (22 slides)

---

## 🎯 Contexte

**Client** : Top 40 fortunes mondiales (~10 milliards €)  
**Projet** : Application "La Voix du Soir" pour ses 2 filles de 8 ans  
**Statut** : **VENDU** — présentation de l'application commandée

### Ce que contient ce dossier

```
Voice/
└── presentation/
    └── index.html    ← La présentation (22 slides)
```

---

## 🚀 Lancer la présentation

```bash
cd presentation
python3 -m http.server 3003
```

Puis ouvrir → **http://localhost:3003**

### Navigation
- **← →** Flèches clavier pour naviguer
- **Points à droite** pour accès direct aux slides
- Scroll automatique **désactivé**

---

## 📊 Structure des 22 slides

| # | Slide | Contenu |
|---|-------|---------|
| 1 | **La Voix du Soir** | Titre + tagline |
| 2 | **Pour Vos Filles** | 4 colonnes : IA, Créer, Publier, Ordinateur |
| 3 | **Les Objectifs** | 6 objectifs pédagogiques avec "Comment" |
| 4 | **Luna, l'Amie IA** | Présentation de Luna (8 ans, guide) |
| 5 | **Luna - Création d'Images** | Dialogue exemple avec les 5 Clés |
| 6 | **Luna - Écriture** | Dialogue exemple avec les 5 Questions |
| 7 | **La Philosophie** | 5 règles de Luna |
| 8 | **5 Clés Magiques** | Synoptique prompting images |
| 9 | **5 Questions Magiques** | Synoptique écriture |
| 10 | **Parcours de Maîtrise** | Niveaux (Explorateur → Maître) |
| 11 | **Cinq Univers Créatifs** | Les 5 modes de l'app |
| 12 | **L'Expérience Théâtre** | AirPlay + Philips Hue |
| 13 | **L'Horizon** | Vision Amazon KDP |
| 14-15 | **Synoptiques techniques** | Prompting & Progression |
| 16-17 | **Design Immersif** | Métaphore livre, animations |
| 18 | **Comment Gemini Fonctionne** | Schéma IA conceptuel |
| 19 | **Multimodal** | Images, Vidéos, Voix |
| 20 | **Tech Stack** | Technologies utilisées |
| 21 | **Fonctionnalités** | Desktop, iPad, Multilingue |
| 22 | **Mon Engagement** | Garanties personnelles |

---

## ✏️ Modifications de la session (15 janvier 2026)

| Action | Détail |
|--------|--------|
| ✅ **Slide 2 refaite** | 4 colonnes visuelles (+ "Maîtriser l'Ordinateur") |
| ✅ **Slide commercial supprimée** | "Prêtes à Créer ?" — déjà vendu |
| ✅ **"Notre" → "Mon"** | Engagement personnel, pas collectif |
| ✅ **26 → 22 slides** | Suppression redondances |

---

## 💡 Points clés pour la cliente

### Ce qu'elle veut entendre

1. **Émotionnel** — C'est pour ses filles, moments en famille
2. **Pédagogique** — Apprentissage IA sérieux (elle connaît l'IA)
3. **Technique** — Jargon OK, justifie le prix/la technicité
4. **Vision** — Ses filles pourront publier un vrai livre

### Ce qu'il ne faut PAS faire

- ❌ Discours commercial (c'est vendu)
- ❌ Simplifier à l'excès (elle connaît l'IA)
- ❌ "Faire de la politique" (être direct)

---

## 🎨 Design de la présentation

### Palette
- **Fond** : Dégradé violet profond (#1a0a2e → #2d1b4e)
- **Accent** : Or (#d4af37)
- **Texte** : Blanc cassé (#f5f5f5)

### Typographies
- **Titres** : Cormorant Garamond (serif élégant)
- **Corps** : Montserrat (sans-serif moderne)

### Effets
- Étoiles animées en arrière-plan
- Animations d'entrée sur chaque slide
- Lune dorée dans le header

---

## 🔗 Lien avec le projet principal

Cette présentation décrit l'application **La Voix du Soir** dont le code source est dans :

```
/Users/gregorymittelette/Dev/lavoixdusoir/
```

La présentation a été **copiée** ici (pas déplacée) — l'original reste dans `lavoixdusoir/presentation/`.

---

## 📝 Pour modifier la présentation

Le fichier `presentation/index.html` contient tout :
- HTML des slides
- CSS intégré (styles, animations)
- JavaScript (navigation, effets)

### Structure d'une slide

```html
<section class="slide stars" data-slide="X">
  <h2 class="animate-in animate-in-1">Titre</h2>
  <p class="animate-in animate-in-2">Contenu...</p>
</section>
```

### Classes utiles
- `.stars` — Ajoute les étoiles animées
- `.animate-in-X` — Animation d'entrée (X = ordre)
- `.feature-card` — Carte avec bordure dorée

---

## ✅ Checklist avant présentation

- [ ] Serveur lancé (`python3 -m http.server 3003`)
- [ ] Navigateur en plein écran (F11 ou Cmd+Shift+F)
- [ ] Commencer à la slide 1 (touche Home)
- [ ] Tester les flèches ← →

---

**Bonne présentation !** 🌙✨
