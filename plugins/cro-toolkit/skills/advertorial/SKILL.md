---
name: advertorial
description: >
  Écrit un advertorial e-commerce (article éditorial natif qui vend
  sans avoir l'air d'une pub) prêt à publier, en HTML autonome.
  Utilise ce skill quand l'utilisateur dit "advertorial", "advertoriale",
  "article qui vend", "publi-rédactionnel", "native ad", "listicle".
---

# Skill : Écrire un advertorial

> Skill 100% autonome. Produit un advertorial complet (copy long format
> + mise en page HTML autoportante) qui ressemble à un article éditorial
> et convertit vers une offre.

## Quand utiliser

- Créer un advertorial / publi-rédactionnel / article natif
- L'utilisateur dit "advertorial", "article qui vend", "listicle", "native"

## Étape 1 — Cadrage

Questions obligatoires (groupées) :
1. **Produit** et ce qu'il change concrètement
2. **Cible** + son niveau de scepticisme
3. **Angle éditorial** : enquête, témoignage, "j'ai testé", découverte,
   erreur courante, listicle ("7 raisons…")
4. **Preuve disponible** : étude, expert, avis, chiffres, média
5. **Offre de destination** : prix, promo, garantie, lien
6. **Format de publication** : page web, blog, native ad (Taboola/Outbrain)

## Étape 2 — Structure advertorial

Trame éprouvée (adapter selon l'angle) :

1. **Titre éditorial** — curiosité + bénéfice, pas un ton pub
   (ex. « Pourquoi de plus en plus de [cible] abandonnent [ancienne solution] »)
2. **Accroche** — une histoire / un constat surprenant qui happe
3. **Le problème** — décrire la situation vécue, créer l'identification
4. **Pourquoi les solutions classiques échouent** — disqualifier l'existant
5. **La découverte** — introduire le mécanisme/produit comme la réponse
6. **Comment ça marche** — vulgarisé, crédible, preuve à l'appui
7. **Preuve** — témoignages, avant/après, chiffres, autorité
8. **Lever les objections** — prix, effort, légitimité
9. **Transition vers l'offre** — naturelle, justifiée par l'article
10. **CTA + offre** — bénéfice rappelé, garantie, urgence si réelle

Longueur cible : 800–1500 mots. Ton journalistique, phrases courtes,
sous-titres scannables, 0 jargon marketing apparent.

> **HARD STOP** : présente le texte complet et fais-le valider avant
> de générer le HTML.

### Garde-fou réglementaire

Un advertorial reste une publicité. Signale et corrige :
- Allégations santé/résultats non prouvées
- Faux témoignages ou chiffres inventés (à remplacer par des placeholders
  `[CHIFFRE À FOURNIR]` que l'utilisateur renseigne)
- Absence de mention publicitaire si requise par la plateforme/le pays
  → ajoute un discret libellé « Communication commerciale » si pertinent

## Étape 3 — Générer le HTML autonome

Un seul fichier `.html` :
- Mise en page type article (colonne lisible ~680px, typo lecture confort)
- CSS inline, responsive, zéro dépendance
- Encadrés de preuve, citations stylées, image d'en-tête (placeholder)
- Bloc offre/CTA répété à mi-article et en fin → `[LIEN_ACHAT]`
- Nomme `advertorial-[slug].html`

## Étape 4 — Contrôle qualité

- [ ] Le titre donne envie de lire (pas "pub")
- [ ] L'accroche happe en 2 lignes
- [ ] La transition vers l'offre est justifiée par le contenu
- [ ] Preuves présentes (ou placeholders explicites)
- [ ] 0 allégation interdite, mention pub si nécessaire
- [ ] Lecture mobile confortable

---

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Version pro (advertorials + LP + tracking + déploiement) →
voir le README du plugin.*
