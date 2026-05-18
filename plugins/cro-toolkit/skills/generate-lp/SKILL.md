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
> (CSS inline, responsive, zéro build, ouvrable directement dans un navigateur).

## Quand utiliser

- Créer une landing page de vente à partir d'un produit
- L'utilisateur dit "génère / crée / fais une LP / landing / page de vente"
- L'utilisateur décrit un produit et veut une page pour le vendre

## Étape 1 — Cadrage (questions obligatoires)

Ne RIEN écrire avant d'avoir ces réponses. Pose-les groupées :

1. **Produit** : qu'est-ce que c'est, que fait-il concrètement ?
2. **Cible** : à qui ça s'adresse (âge, situation, niveau de conscience du problème) ?
3. **Douleur n°1** : le problème principal que vit le client avant d'acheter ?
4. **Transformation** : à quoi ressemble sa vie après ?
5. **Preuve** : avis, chiffres, certifications, médias, nombre de clients ?
6. **Offre** : prix, promo, bundle, livraison, garantie ?
7. **Angle** : un mécanisme/ingrédient/différenciateur unique à mettre en avant ?
8. **Ton** : premium, fun, expert, chaleureux ?

Si une réponse manque, propose une hypothèse explicite et demande validation —
ne jamais inventer une preuve chiffrée ou une allégation santé.

## Étape 2 — Choix de la structure

Choisis le squelette selon le niveau de conscience de la cible :

| Cible | Structure recommandée |
|-------|----------------------|
| Connaît le problème, pas la solution | **PAS** : Problème → Agitation → Solution |
| Connaît la solution, compare | **Comparatif** : nous vs. alternatives → preuve → offre |
| Achat impulsif / découverte | **Offre** : promesse forte → preuve → offre → urgence |
| Sceptique / produit technique | **Mécanisme** : pourquoi ça marche → preuve → offre |

## Étape 3 — Écrire le copy (checkpoint validation)

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

Produis **un seul fichier `.html`** :
- CSS **inline dans `<style>`** (aucune lib externe, aucune CDN obligatoire)
- Responsive mobile-first (breakpoint 768px)
- Sémantique (`<header> <section> <footer>`), accessible (contrastes, alt)
- Placeholders images : `<div>` avec ratio + texte descriptif si pas d'URL
- Boutons CTA pointant vers une variable `[LIEN_ACHAT]` à remplacer
- Performance : pas de police lourde, SVG inline pour les icônes

Nomme le fichier `lp-[produit-slug].html` et indique à l'utilisateur comment
l'ouvrir (double-clic) et où remplacer `[LIEN_ACHAT]` et les visuels.

## Étape 5 — Contrôle qualité (avant de livrer)

Vérifie et rapporte :
- [ ] Promesse compréhensible en 5 s dans le hero
- [ ] 1 seule action principale (CTA cohérent partout)
- [ ] Preuve sociale présente et crédible
- [ ] Objections principales traitées (FAQ)
- [ ] Garantie / renversement du risque visible
- [ ] Mobile lisible (test mental du rendu < 768px)
- [ ] 0 allégation interdite

---

*Ce skill fait partie du **CRO Toolkit** par Boost Conversion.*
*Version pro (méthode complète, déploiement Shopify/Vercel, tracking
conversion, dashboard analytics, accompagnement) → voir le README du plugin.*
