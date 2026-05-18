---
name: analyze-reviews
description: >
  Analyse des avis clients pour en extraire les angles marketing, les
  objections et le vocabulaire réel à réutiliser dans le copy. Utilise
  ce skill quand l'utilisateur dit "avis", "reviews", "analyse les avis",
  "verbatims", ou fournit un export d'avis (CSV/texte).
---

# Skill : Analyser les avis clients

> Skill 100% autonome. Transforme un paquet d'avis en angles de vente,
> objections et verbatims prêts à coller dans une LP ou un advertorial.

## Quand utiliser

- Extraire des insights d'avis clients
- L'utilisateur dit "analyse les avis / reviews / verbatims"
- Avant de générer une LP, pour nourrir le copy avec les vrais mots clients

## Étape 1 — Récupérer les avis

Demande la source : **CSV/export collé**, fichier fourni, ou copier-coller
de texte. Colonnes utiles si dispo : note, texte, produit, date.
Si > 100 avis, échantillonne intelligemment (mix de notes hautes ET basses,
pas seulement les 5 étoiles).

## Étape 2 — Coder les avis

Classe chaque avis selon :
- **Note** (positif / mitigé / négatif)
- **Thème** (résultat, qualité, prix, livraison, SAV, usage, packaging…)
- **Bénéfice cité** (ce qui a plu — la transformation réelle)
- **Objection / friction** (ce qui a déçu ou inquiété avant l'achat)
- **Déclencheur d'achat** (pourquoi ils ont acheté — si mentionné)

## Étape 3 — Synthèse exploitable

Restitue dans ce format :

```
ANGLES DE VENTE (par fréquence)
1. [Bénéfice dominant] — cité dans ~X% des avis positifs
   Verbatim : « ... » (note)
2. ...

OBJECTIONS À LEVER DANS LE COPY
- [Objection] — fréquence — comment la traiter sur la page
- ...

VOCABULAIRE CLIENT (à réutiliser tel quel)
- Mots/expressions récurrents : "...", "...", "..."
  (utiliser ces formulations dans les titres et la FAQ)

DÉCLENCHEURS D'ACHAT
- ...

PREUVES À AFFICHER (verbatims les plus forts, prêts à coller)
- « ... » — [prénom si dispo], [note]
- ...

SIGNAUX FAIBLES / RISQUES
- Problèmes récurrents à NE PAS masquer mais désamorcer
```

Règles : citer des verbatims réels (ne jamais inventer un avis) ; pondérer
par fréquence, pas par anecdote ; remonter aussi les signaux négatifs
(ils nourrissent la FAQ et la garantie).

## Étape 4 — Proposer la suite

Termine par : « Tu veux que j'utilise ces angles pour générer une LP
ou un advertorial ? » (→ `generate-lp` / `advertorial`).

---

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Analyse d'avis à grande échelle + intégration directe au copy en
version pro → voir le README du plugin.*
