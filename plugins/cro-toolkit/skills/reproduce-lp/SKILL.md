---
name: reproduce-lp
description: >
  Reproduit fidèlement une landing page existante à partir d'une URL,
  d'un HTML source ou de screenshots, en un fichier HTML autonome.
  Utilise ce skill quand l'utilisateur dit "reproduis", "clone",
  "duplique", "refais à l'identique" + "lp", "landing", "page",
  ou fournit une URL/capture à reproduire.
---

# Skill : Reproduire une landing page

> Skill 100% autonome. Reproduction section par section avec validation
> à chaque étape. Source de vérité = URL live, HTML fourni, ou screenshots.
> Sortie = un fichier `.html` autoportant.

## Quand utiliser

- Recréer une LP existante (URL, HTML, ou captures)
- L'utilisateur dit "reproduis / clone / duplique / refais à l'identique"
- L'utilisateur fournit une URL + "pars de cette page"

**NE PAS utiliser pour** : créer une LP de zéro (→ `generate-lp`),
auditer (→ `cro-audit`).

## Étape 1 — Récupérer la source

Demande à l'utilisateur **une** de ces sources :
- Une **URL** → récupère le HTML rendu (WebFetch) + décris la structure
- Le **HTML source** collé
- Des **screenshots** (desktop + mobile si possible)

Précise le périmètre : reproduction *fidèle* (1:1) ou *adaptation*
(même structure, contenu/marque différents) ? Demande la nouvelle marque,
les nouveaux textes et le produit si c'est une adaptation.

## Étape 2 — Découper en sections

Liste les sections détectées dans l'ordre, ex. :
`Hero → Réassurance → Problème → Bénéfices → Preuve → Offre → FAQ → Footer`

Présente cette liste et fais-la valider avant de coder.

## Étape 3 — Reproduire section par section

Pour **chaque** section, dans l'ordre :
1. Décris ce que tu observes (layout, hiérarchie, couleurs, espacements)
2. Reproduis-la en HTML/CSS inline autonome
3. Montre le code de la section + un rendu décrit
4. Demande validation avant de passer à la suivante

Ne jamais tout produire d'un coup : une section cassée se corrige avant
de continuer. Conserve la grille, la typo et les couleurs de la source
(extrais les valeurs hex/spacing observées).

### Garde-fou contenu

Si c'est une adaptation marque : remplace tous les textes/visuels par ceux
du nouveau produit, ne copie aucune allégation non vérifiable, ne reprends
aucun élément de marque protégé (logo, nom) du modèle d'origine.

## Étape 4 — Assembler et livrer

- Assemble les sections validées en **un seul `.html`** autonome
- CSS inline, responsive (breakpoint 768px), zéro dépendance externe
- Placeholders pour les images manquantes (ratio + description)
- CTA → variable `[LIEN_ACHAT]` à remplacer
- Nomme `lp-reproduction-[slug].html` et explique comment l'ouvrir

## Étape 5 — Contrôle de fidélité

Rapporte les écarts assumés vs. la source :
- [ ] Structure des sections identique
- [ ] Hiérarchie visuelle respectée (tailles, poids, ordre)
- [ ] Palette et typo cohérentes
- [ ] Responsive fonctionnel
- [ ] Écarts volontaires listés et justifiés

---

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Version pro (clonage avec déploiement, tracking, accompagnement) →
voir le README du plugin.*
