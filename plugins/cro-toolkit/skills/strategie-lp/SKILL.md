---
name: strategie-lp
description: >
  Diagnostique le niveau de conscience d'une audience cible et recommande
  le type de landing page optimal, les sections à inclure et leur ordre,
  avant toute rédaction. Basé sur la pyramide de conscience Schwartz et
  la Phase 4 de la Méthode Océan Vert. Utilise ce skill quand l'utilisateur
  dit "quelle LP faire", "par où commencer", "quel type de page", "stratégie
  landing page", ou AVANT d'utiliser generate-lp, advertorial ou listicle.
---

# Skill : Choisir la bonne stratégie de landing page (Méthode Océan Vert)

> Skill 100% autonome. Répond à la question que tout e-commerçant se pose
> avant de créer une page : **"Quel type de LP dois-je construire pour
> CE canal, avec CETTE audience ?"**
>
> Sortie = un **Brief Stratégique LP** complet prêt à coller dans
> `generate-lp`, `advertorial` ou `listicle`.
>
> **Principe Océan Vert :** Une LP qui ne correspond pas au niveau de
> conscience de son audience ne peut pas convertir, peu importe la qualité
> du copy. C'est l'étape 0 avant toute création.

## Quand utiliser

- Avant de créer une LP (toujours idéalement)
- L'utilisateur ne sait pas quel type de page construire
- Nouvelle campagne sur un canal non encore testé
- La LP existante ne convertit pas → diagnostiquer le problème de ciblage

> **Dossier Prospect (optionnel)** : si `ocean-vert-prospect.md` existe,
> lis-le — le niveau de conscience et le brief y sont pré-remplis.
> Sans ce fichier, ce skill fonctionne de façon entièrement autonome.

**Utiliser AVANT :** `generate-lp` · `advertorial` · `listicle`
**Utiliser APRÈS :** `offre` · `recherche-prospect`

---

## Étape 1 — Cadrage rapide (3 questions)

Pose ces 3 questions groupées — elles suffisent pour le diagnostic :

1. **Produit** : que vend-on et quelle est la transformation principale ?
2. **Canal d'acquisition** : d'où vient ce trafic ?
   - Pub froide (Meta, TikTok, Display) — audience qui ne vous connaît pas
   - Search payant (Google Ads, Shopping) — audience qui cherche activement
   - SEO organique — audience qui cherche une information ou une solution
   - Email liste froide — audience segmentée mais pas encore qualifiée
   - Email liste chaude / retargeting — audience qui vous connaît déjà
   - Recommandation / bouche-à-oreille
3. **Ce que la cible sait déjà** (si connu) : sait-elle qu'elle a un problème ?
   Connaît-elle votre type de produit ? Connaît-elle votre marque ?

---

## Étape 2 — Diagnostiquer le niveau de conscience

Utilise les réponses pour situer l'audience sur la **pyramide Schwartz à 5 niveaux**.
Si l'utilisateur ne sait pas, infère depuis le canal (voir tableau de défaut ci-dessous).

### Les 5 niveaux et leurs signaux

| Niveau | Ce que la cible sait | Signaux typiques |
|--------|---------------------|-----------------|
| **1 — Non-consciente** | Ignore le problème ET la solution | Pub interruptive, audience froide large, aucune recherche active |
| **2 — Consciente du problème** | Sait qu'elle souffre, ne sait pas comment résoudre | Recherches génériques ("comment perdre du ventre"), audience intérêt large |
| **3 — Consciente de la solution** | Connaît des solutions, compare les options | Recherches comparatives ("meilleur complément minceur"), remarketing concurrent |
| **4 — Consciente de la marque** | Vous connaît, hésite encore | A visité votre site, est abonnée à votre newsletter, connaît votre produit |
| **5 — Prête à acheter** | A déjà vu l'offre, a besoin d'un déclencheur final | A ajouté au panier, a visité la page offre, est client existant |

### Mapping canal → niveau de conscience par défaut

| Canal | Niveau probable | Raison |
|-------|----------------|--------|
| Meta / TikTok cold (intérêts larges) | 1–2 | Interruption — la cible ne cherchait pas |
| Meta / TikTok retargeting | 4–5 | A déjà interagi avec la marque |
| Google Search générique | 2–3 | Cherche une solution, pas encore votre marque |
| Google Search marque | 4–5 | Cherche spécifiquement votre nom |
| Google Shopping | 3–4 | Compare activement les produits |
| SEO article de blog | 2–3 | Cherche une information / solution |
| Email liste froide | 2 | Segmentée mais pas encore engagée |
| Email liste chaude | 4 | Engagée, connaît votre valeur |
| Bouche-à-oreille / recommandation | 3–4 | Confiance transférée, compare encore |

**Annonce le niveau diagnostiqué et sa justification** avant de continuer.

---

## Étape 3 — Recommander le type de LP

### Correspondance niveau × type de LP

| Niveau | Type de LP recommandé (principal) | Alternatives | Logique |
|--------|----------------------------------|--------------|---------|
| **1 — Non-consciente** | **Advertorial** ou **Listicle** | VSL | Éduquer d'abord : nommer l'ennemi, révéler le problème, introduire la solution progressivement |
| **2 — Consciente du problème** | **Success Story** ou **Éducatif long** | Quiz, Advertorial court | Montrer que la solution existe et qu'elle marche pour quelqu'un comme eux |
| **3 — Consciente de la solution** | **Comparatif** ou **Mécanisme unique** | Success Story avec comparaison | Gagner la comparaison : pourquoi vous plutôt qu'eux |
| **4 — Consciente de la marque** | **Offre** ou **Bundle** | Comparatif simplifié | Lever le dernier frein : l'offre, la garantie, la preuve finale |
| **5 — Prête à acheter** | **Retargeting offre simple** | Offre + urgence | Un seul objectif : déclencher l'achat maintenant |

### Signaux d'alerte

⚠️ **Erreur classique n°1** : envoyer du trafic Meta froid (niveau 1) vers une LP "Offre"
→ La cible ne comprend pas pourquoi acheter, le prix paraît injustifié, le taux de rebond explose

⚠️ **Erreur classique n°2** : envoyer du trafic Search bas de funnel (niveau 4-5) vers un advertorial long
→ La cible veut acheter, pas lire un article — la friction tue la conversion

---

## Étape 4 — Composer le puzzle des sections

Pour le type de LP recommandé, donne la liste des sections à inclure dans l'ordre.

### Sections par type de LP

#### Advertorial / Listicle (niveau 1–2)
Objectif : éduquer et créer la confiance avant de vendre.

```
1. Titre éditorial (accroche ennemi ou révélation)
2. Intro identification (2-3 phrases : "si vous êtes [cible]...")
3. Problème / Agitation (nommer la douleur avec leurs mots)
4. Ennemi commun (à qui la faute — pas au lecteur)
5. Pourquoi les solutions classiques ont échoué
6. Découverte / Mécanisme (introduire le produit comme la réponse)
7. Comment ça marche (vulgarisé, crédible)
8. Preuve — expert / étude / chiffre
9. Témoignage transformation (avant/après narratif)
10. Transition offre (naturelle, justifiée par l'article)
11. Stack offre + bonus
12. Garantie
13. CTA (bénéfice, pas "Acheter")
14. FAQ (3-4 objections traitées)
```

#### Success Story (niveau 2)
Objectif : prouver que quelqu'un comme eux a réussi.

```
1. Hero — promesse de transformation + preuve chiffrée
2. Présentation du héros (client relatable — situation de départ identique)
3. Le problème vécu (détail émotionnel)
4. Ce qu'il a essayé sans succès (justifier les échecs passés)
5. La découverte (comment il a trouvé la solution)
6. La transformation — résultat précis avec délai
7. Mécanisme expliqué (pourquoi ça a marché pour lui)
8. Autres témoignages similaires (pattern de succès)
9. Offre + garantie
10. CTA
11. FAQ (objections "est-ce que ça marcherait pour moi ?")
```

#### Comparatif (niveau 3)
Objectif : gagner la comparaison sans dénigrer.

```
1. Hero — proposition de valeur unique (ce que les autres ne font pas)
2. Barre de réassurance (chiffres de confiance)
3. Tableau comparatif (vous vs alternatives — critères choisis stratégiquement)
4. Explication du mécanisme différenciateur
5. Bénéfices exclusifs (ce que seul vous offrez)
6. Preuve sociale (avis ciblés sur les points de différence)
7. Offre + stack bonus
8. Garantie (plus forte que la concurrence si possible)
9. FAQ (objections de comparaison : prix, efficacité, service)
10. CTA
```

#### Offre / Bundle (niveau 4)
Objectif : convaincre sur l'offre, lever le dernier frein.

```
1. Hero offre — promesse + offre visible immédiatement
2. Barre de réassurance (livraison, garantie, avis)
3. Stack offre détaillé (produit + bonus nommés et valorisés)
4. Preuve sociale récente (avis datés — la fraîcheur rassure)
5. Urgence / rareté (si réelle)
6. Garantie en détail
7. FAQ courte (3-4 objections : livraison, retour, paiement)
8. CTA répété (≥ 3 fois : hero, mi-page, fin)
```

#### Retargeting (niveau 5)
Objectif : un seul message, une seule action.

```
1. Hero minimaliste — rappel de l'offre + déclencheur final
   (ex : "Vous avez failli craquer. Voici pourquoi c'était la bonne décision.")
2. Dernier argument manquant (celui qui manquait lors de la première visite)
3. Preuve sociale ciblée (avis qui répond à l'objection probable)
4. Garantie mise en avant
5. Urgence (si applicable)
6. CTA unique et direct
```

---

## Étape 5 — Livrer le Brief Stratégique LP

Produis ce document structuré en sortie :

```
╔══════════════════════════════════════════════╗
  BRIEF STRATÉGIQUE LP — [Produit]
╚══════════════════════════════════════════════╝

DIAGNOSTIC AUDIENCE
→ Canal : [canal]
→ Niveau de conscience : [N] — [Non-consciente / Consciente du problème / ...]
→ Justification : [pourquoi ce niveau]

TYPE DE LP RECOMMANDÉ
→ [Type principal]
→ Pourquoi : [logique en 1 phrase]
→ Alternative si budget limité : [type simplifié]

SECTIONS RECOMMANDÉES (dans l'ordre)
1. [Section] — [rôle en 5 mots]
2. [Section] — [rôle en 5 mots]
[...]

TON ET ANGLE
→ Registre : [journalistique / direct / intime / expert]
→ Angle d'accroche : [ennemi / révélation / comparaison / offre]
→ Longueur estimée : [X mots / X sections]

POUR EXÉCUTER CE BRIEF
→ Lance `[skill]` avec ce brief comme contexte
→ Si tu n'as pas encore les avis clients : lance d'abord `analyze-reviews`
→ Si l'offre n'est pas structurée : lance d'abord `offre`

POINTS DE VIGILANCE
→ [Erreur à éviter pour ce niveau / canal]
→ [Élément critique pour ce type de LP]
╔══════════════════════════════════════════════╝
```

---

**Enchaîner :** `generate-lp` · `advertorial` · `listicle` (selon le type recommandé) · `offre` (si le stack n'est pas encore construit) · `analyze-reviews` (si les avis ne sont pas encore analysés).

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion — Méthode Océan Vert.*
*Phase 4 complète (templates Figma, 26 sections détaillées, intégration Unbounce) → version pro.*
