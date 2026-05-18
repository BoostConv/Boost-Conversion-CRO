---
name: cro-audit
description: >
  Audite une landing page ou une page produit e-commerce et renvoie un
  score /100 + un plan d'action priorisé. Utilise ce skill quand
  l'utilisateur dit "audit", "audite", "analyse cette page", "score CRO",
  "pourquoi ça ne convertit pas", ou fournit une URL/HTML à évaluer.
---

# Skill : Auditer une page (score CRO /100)

> Skill 100% autonome. Évalue une page contre une grille CRO générique
> et renvoie un score chiffré + les correctifs priorisés par impact.

## Quand utiliser

- Évaluer une LP / page produit existante
- L'utilisateur dit "audit", "score CRO", "pourquoi ça ne convertit pas"
- L'utilisateur fournit une URL, un HTML, ou des screenshots

## Étape 1 — Récupérer la page

Demande **une** source : URL (récupère le rendu via WebFetch), HTML collé,
ou screenshots desktop + mobile. Demande aussi le **contexte** : produit,
cible, canal d'acquisition, et l'objectif (achat, lead, RDV).

## Étape 2 — Grille d'audit (100 points)

Note chaque critère, justifie, cite l'élément concerné :

| Bloc | Critères | Points |
|------|----------|--------|
| **Clarté (20)** | Promesse comprise en 5 s ; pour qui ; proposition de valeur unique | /20 |
| **Hero & CTA (15)** | CTA visible above the fold ; libellé orienté bénéfice ; 1 action principale | /15 |
| **Preuve sociale (15)** | Avis crédibles ; chiffres ; UGC/avant-après ; autorité | /15 |
| **Offre & risque (15)** | Offre claire ; prix justifié ; garantie / renversement du risque | /15 |
| **Objections (10)** | FAQ ; objections prix/délai/efficacité traitées | /10 |
| **Friction (10)** | Parcours court ; formulaire minimal ; pas de distraction | /10 |
| **Mobile & vitesse (10)** | Lisible < 768px ; CTA accessible ; pas de blocage perçu | /10 |
| **Confiance (5)** | Mentions légales, paiement, contact, cohérence visuelle | /5 |

Score total = somme. Barème : **< 60** critique · **60-74** à risque ·
**75-84** correct · **85-100** fort.

## Étape 3 — Restituer

Format de sortie :

```
SCORE CRO : XX/100  —  [niveau]

TOP 3 LEVIERS (par impact estimé)
1. [Problème] → [Correctif concret] → impact attendu : élevé
2. ...
3. ...

DÉTAIL PAR BLOC
- Clarté : 14/20 — [ce qui va / ne va pas, élément cité]
- Hero & CTA : ...
[...]

QUICK WINS (< 30 min)
- ...

CHANTIERS (refonte partielle)
- ...
```

Règles : chaque reproche est **actionnable** (dire quoi changer, pas juste
"à améliorer"). Prioriser par impact x effort. Ne jamais inventer de
données analytics : raisonner sur ce qui est observable sur la page.

## Étape 4 — Proposer la suite

Termine par : « Tu veux que je réécrive la/les section(s) faibles, ou que
je régénère la page complète corrigée ? » (→ enchaîne sur `generate-lp`
ou `reproduce-lp` si l'utilisateur valide).

---

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Audit approfondi avec données réelles (heatmaps, tracking conversion,
A/B tests) en version pro → voir le README du plugin.*
