# DIGITAL SUPPORT TECH — Site officiel

Site web premium de l'entreprise **Digital Support Tech**, spécialisée en support technique, maintenance informatique, dépannage Windows, installation de logiciels, optimisation PC, sécurité et récupération de données.

> Design inspiré de Microsoft, Dell Support, Apple, Cisco, Malwarebytes et Kaspersky.

---

## 🚀 Démarrage rapide

Le site est livré en **un seul fichier** (`index.html`) optimisé pour la performance :

- Ouvrez simplement `index.html` dans un navigateur, **ou**
- Servez-le via un serveur local : `python -m http.server` puis `http://localhost:8000`

Aucune dépendance à installer : Bootstrap 5, Bootstrap Icons et les polices Sora/Inter sont chargés via CDN.

---

## 🗂 Arborescence cible (architecture professionnelle)

Le livrable est un fichier unique pour des raisons de simplicité de déploiement et de performance (zéro requête statique). L'architecture de production recommandée est la suivante :

```
digitalsupporttech/
├── index.html                  ← Livrable actuel (SPA complète)
├── README.md
├── assets/
│   ├── css/
│   │   └── style.css           ← Extraire le <style> du head
│   ├── js/
│   │   ├── data.js             ← Données (services, guides, blog…)
│   │   ├── router.js           ← Routeur hash SPA
│   │   └── app.js              ← Animations & interactions
│   ├── images/
│   │   ├── hero-illustration.svg
│   │   └── blog/               ← Visuels des articles
│   ├── icons/                  ← Favicon, icônes SVG
│   └── fonts/                  ← Polices auto-hébergées (optionnel)
├── pages/
│   ├── index.html
│   ├── services.html
│   ├── diagnostic.html
│   ├── guides.html
│   ├── blog.html
│   ├── telechargements.html
│   ├── faq.html
│   ├── apropos.html
│   ├── contact.html
│   ├── confidentialite.html
│   └── conditions.html
└── components/
    ├── navbar.html
    ├── footer.html
    └── modals.html
```

> Pour une version multi-fichiers (meilleure pour le SEO par page), chaque `<section class="page">` peut être extraite dans `pages/*.html` en conservant le routeur.

---

## 🎨 Design system

| Élément | Valeur |
|---|---|
| Bleu principal | `#0057D9` |
| Bleu clair | `#2EA8FF` |
| Bleu foncé | `#0A2D6B` |
| Fond clair | `#F4F7FB` |
| Texte | `#0B1B33` / `#5B6B85` |
| Titres | Sora (Google Fonts) |
| Corps | Inter (Google Fonts) |
| Radius | 18–26 px |
| Ombres | Douces, bleutées, multi-couches |

---

## 📄 Pages (11)

1. **Accueil** — Hero premium, illustration (ordinateur / Windows / réseau / sécurité), statistiques animées, services, processus, atouts, témoignages, blog, CTA.
2. **Services** — 9 cartes premium avec icônes, avantages et modal « En savoir plus ».
3. **Diagnostic** — Outil interactif : 8 problèmes, mini-diagnostic pas à pas, causes probables, solutions, CTA contact pré-rempli.
4. **Guides** — Bibliothèque de 14 tutoriels, 6 catégories, recherche instantanée.
5. **Blog** — 9 articles, images, catégories, pagination, sidebar (catégories + populaires).
6. **Téléchargements** — 12 logiciels (Windows, Office, AnyDesk, UltraViewer, Chrome, Firefox, 7-Zip, Adobe Reader, VLC, pilotes, outils Microsoft), recherche + filtres.
7. **FAQ** — 12 questions en accordéon Bootstrap.
8. **À propos** — Histoire, valeurs, chronologie, certifications.
9. **Contact** — Formulaire validé, carte Google Maps, WhatsApp, email, horaires, bouton WhatsApp flottant.
10. **Politique de confidentialité** — Conforme RGPD.
11. **Conditions d'utilisation** — CGU.

---

## ⚙️ Fonctionnalités techniques

- **SPA multi-pages** via routeur hash (`#/services`, `#/contact?sujet=...`)
- **Animations** : fade / slide / zoom au scroll (IntersectionObserver), compteurs animés, hover premium, boutons avec effet de brillance, blobs et illustration flottante
- **Glassmorphism** : navbar, cartes statistiques, badges
- **SEO** : meta title/description, Open Graph, Twitter Card, JSON-LD (ProfessionalService + FAQPage), balises ALT, hiérarchie H1→H3, sémantique HTML5
- **Accessibilité** : skip-link, ARIA, focus visible, `prefers-reduced-motion`, contrastes
- **Responsive** : mobile-first, menu off-canvas, grilles adaptatives
- **Performance** : chargement différé des images (`loading="lazy"`), CSS minifié à la demande, aucune bibliothèque superflue

---

## 🧭 Personnalisation rapide

| À modifier | Emplacement |
|---|---|
| Téléphone / WhatsApp | Rechercher `33600000000` |
| Email | Rechercher `contact@digitalsupporttech.fr` |
| Adresse / zone | Page contact + footer |
| Réseaux sociaux | Footer (`social`) + JSON-LD `sameAs` |
| Coordonnées Google Maps | Lien `maps.google.com/?q=Paris` |
| Contenus | Constantes JS `SERVICES`, `DIAGNOSTICS`, `GUIDES`, `POSTS`, `DOWNLOADS`, `FAQS` |

---

© Digital Support Tech — Tous droits réservés.
