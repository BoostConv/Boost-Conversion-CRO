---
name: generate-lp
description: >
  Génère une landing page e-commerce haute conversion de A à Z, en
  HTML autonome (un seul fichier, aucune dépendance). Utilise ce skill
  quand l'utilisateur dit "génère", "crée", "fais", "nouvelle" +
  "lp", "landing", "page de vente", ou décrit un produit à vendre.
---

# Skill : Générer une landing page haute conversion

> Skill 100% autonome. Aucune lecture de fichier projet : tout le contexte
> est demandé à l'utilisateur. Sortie = un fichier `.html` autoportant
> (CSS inline, responsive, CTA sticky mobile, zéro build).
>
> **Mode rapide** : si l'utilisateur ajoute `--fast` ou dit "sans validation",
> saute les checkpoints de validation (Étapes 3 et 4) et livre directement.

## Quand utiliser

- Créer une landing page de vente à partir d'un produit
- L'utilisateur dit "génère / crée / fais une LP / landing / page de vente"
- L'utilisateur décrit un produit et veut une page pour le vendre

> **Dossier Prospect (optionnel)** : si `ocean-vert-prospect.md` existe
> dans le projet, lis-le — il remplace la plupart des questions de l'Étape 1.
> Sans ce fichier, ce skill fonctionne de façon entièrement autonome.

## Étape 1 — Cadrage (questions obligatoires + optionnelles)

Ne RIEN écrire avant d'avoir les réponses essentielles.

### Questions essentielles (pose-les groupées — sans ces 4, impossible de continuer)

1. **Produit** : qu'est-ce que c'est, que fait-il concrètement ?
2. **Cible** : à qui ça s'adresse (situation, niveau de conscience du problème) ?
3. **Douleur n°1** : le problème principal que vit le client avant d'acheter ?
4. **Offre** : prix, promo, bundle, livraison, garantie ?

### Questions optionnelles (si non fournies, utilise les valeurs par défaut ci-dessous)

| Question | Valeur par défaut si absent |
|---|---|
| **Transformation** : à quoi ressemble la vie après ? | Déduite du produit + douleur |
| **Preuve** : avis, chiffres, certifications, médias ? | Section preuve avec placeholders `[AVIS À AJOUTER]` |
| **Angle** : mécanisme/ingrédient/différenciateur unique ? | Bénéfice principal du produit |
| **Ton** : premium, fun, expert, chaleureux ? | Neutre/professionnel |

Signale à l'utilisateur les valeurs par défaut utilisées — ne jamais inventer
une preuve chiffrée ou une allégation santé.

## Étape 2 — Choix de la structure

Choisis le squelette selon le niveau de conscience de la cible :

| Cible | Structure recommandée |
|-------|----------------------|
| Connaît le problème, pas la solution | **PAS** : Problème → Agitation → Solution |
| Connaît la solution, compare | **Comparatif** : nous vs. alternatives → preuve → offre |
| Achat impulsif / découverte | **Offre** : promesse forte → preuve → offre → urgence |
| Sceptique / produit technique | **Mécanisme** : pourquoi ça marche → preuve → offre |

## Étape 3 — Écrire le copy (checkpoint validation)

> **Mode rapide** : si `--fast`, saute ce checkpoint et passe directement à l'Étape 4.

Rédige le copy section par section selon l'anatomie haute conversion :

1. **Hero** — promesse claire (bénéfice + délai) + sous-titre + CTA + visuel.
   Règle : le visiteur doit comprendre quoi/pour qui/pourquoi en 5 secondes.
2. **Barre de réassurance** — 3-4 micro-preuves (livraison, garantie, nb clients).
3. **Problème / Agitation** — décrire la douleur avec les mots du client.
4. **Solution / Mécanisme** — comment le produit résout, pourquoi c'est crédible.
5. **Bénéfices** — 3 à 6 blocs *bénéfice* (pas *fonctionnalité*).
6. **Preuve sociale** — avis verbatim, avant/après, UGC, chiffres, logos.
7. **Offre** — ce qu'on reçoit, prix barré, bonus, livraison.
8. **Renversement du risque** — garantie claire, sans jargon.
9. **Urgence / rareté** — uniquement si vraie (stock, deadline réelle).
10. **FAQ** — 5-6 objections traitées (prix, délai, efficacité, retour).
11. **CTA final** — rappel promesse + bouton.

> **HARD STOP** : présente le copy complet dans un bloc formaté et demande
> « Valide le copy avant que je génère le code. Tu veux modifier quelque
> chose ? ». Ne génère pas le HTML sans « OK » explicite.

### Garde-fou réglementaire (automatique)

Avant de présenter le copy, relis-le et signale tout :
- Allégation santé/thérapeutique non prouvée (« guérit », « soigne »)
- Superlatif non étayé (« le meilleur », « n°1 ») sans source
- Promesse de résultat garanti irréaliste

Propose une reformulation conforme et signale-la à l'utilisateur.

## Étape 4 — Générer le HTML autonome

> **Mode rapide** : si `--fast`, génère directement sans attendre de validation copy.

Produis **un seul fichier `.html`** :
- **`<head>` complet** :
  - `<title>[Promesse principale du hero]</title>`
  - `<meta name="description" content="[Bénéfice + cible + offre en 150 car.]">`
  - `<meta charset="UTF-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1">`
- CSS **inline dans `<style>`** (aucune lib externe, aucune CDN obligatoire)
- Responsive mobile-first (breakpoint 768px)
- **CTA sticky sur mobile** : `position: fixed; bottom: 0;` visible uniquement sous 768px,
  disparaît si le hero est visible à l'écran (évite la double lecture)
- Sémantique (`<header> <section> <footer>`), accessible (contrastes, alt)
- Placeholders images : `<div>` avec ratio + texte descriptif si pas d'URL
- Boutons CTA pointant vers une variable `[LIEN_ACHAT]` à remplacer
- Performance : pas de police lourde, SVG inline pour les icônes

Nomme le fichier `lp-[produit-slug].html` et indique à l'utilisateur :
1. Comment l'ouvrir (double-clic)
2. Où remplacer `[LIEN_ACHAT]` et les visuels
3. Que `<title>` et `<meta description>` sont pré-remplis mais à ajuster

## Étape 5 — Contrôle qualité (avant de livrer)

Vérifie et rapporte :
- [ ] Promesse compréhensible en 5 s dans le hero
- [ ] 1 seule action principale (CTA cohérent partout)
- [ ] CTA sticky mobile présent et non intrusif
- [ ] `<title>` et `<meta description>` renseignés
- [ ] Preuve sociale présente (ou placeholders explicites)
- [ ] Objections principales traitées (FAQ)
- [ ] Garantie / renversement du risque visible
- [ ] Mobile lisible (test mental du rendu < 768px)
- [ ] 0 allégation interdite

---

**Enchaîner :** `cro-audit` pour scorer la page livrée · `analyze-reviews` si tu veux améliorer le copy avec de vrais verbatims clients.

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Version pro (méthode complète, déploiement Shopify/Vercel, tracking
conversion, dashboard analytics, accompagnement) → voir le README du plugin.*
