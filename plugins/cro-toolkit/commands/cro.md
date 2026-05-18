---
description: Menu du CRO Toolkit — affiche les skills disponibles et oriente vers le bon
---

Affiche ce menu à l'utilisateur, puis demande-lui ce qu'il veut faire et
enchaîne sur le skill correspondant.

```
CRO TOOLKIT — par Boost Conversion

  1. generate-lp       Générer une landing page haute conversion (HTML autonome)
  2. reproduce-lp      Cloner / adapter une LP existante depuis une URL
  3. advertorial       Écrire un advertorial éditorial qui vend
  4. cro-audit         Auditer une page → score /100 + plan d'action
  5. analyze-reviews   Extraire angles & objections des avis clients

Dis-moi : un numéro, le nom du skill, ou décris directement ton besoin
(ex. « génère une LP pour ma crème solaire bio »).
```

Si l'utilisateur a donné son besoin dans `$ARGUMENTS`, ne montre pas le
menu : route directement vers le skill le plus pertinent.
