# SprintForge Design System

Référence visuelle extraite de la landing page Aura Builder. Les valeurs sont des repères à réutiliser, pas des contraintes absolues.

## Identité

- **Ambiance :** studio produit haut de gamme, surfaces claires légèrement grises, contrastes noirs et touches orange-rouge.
- **Formes :** grandes capsules pour les boutons et badges, cartes très arrondies (24 à 40 px), bordures discrètes.
- **Profondeur :** ombres diffuses, reflets blancs internes, fonds translucides avec flou pour la navigation.

## Couleurs

| Rôle | Valeur | Usage |
| --- | --- | --- |
| Fond global | `#ECEDEE` | Fond de page |
| Surface claire | `#F4F5F5` | Hero, fonds secondaires |
| Surface chaude | `#F7F7F5` | Panneaux et zones mises en avant |
| Blanc | `#FFFFFF` | Cartes et champs |
| Encre | `#171719` | Boutons principaux et panneaux sombres |
| Titres | `#2E3034` | Titres sur fond clair |
| Texte secondaire | `#55575C` | Paragraphes et navigation |
| Texte discret | `#8A8C91` | Métadonnées, légendes |
| Accent | `#E34A32` | Liens, icônes et repères principaux |
| Accent lumineux | `#F05A3C` | Dégradés et accent sur fond sombre |

Variables disponibles dans `src/styles/global.css` : `--bg`, `--surface`, `--paper`, `--ink`, `--heading`, `--muted`, `--quiet`, `--accent` et `--accent-light`.

## Typographie

- **Inter** pour l’interface, les paragraphes, les libellés et les titres standards. Graisses utilisées : 400, 500, 600 et 700.
- **Instrument Serif** en italique pour un accent expressif dans le titre du hero.
- Titres fortement resserrés (`letter-spacing` proche de `-0.05em`), interligne compact de 1.0 à 1.1.
- Paragraphes : 14 à 18 px, interligne de 1.6 à 1.75.
- Les petites légendes sont en 10 à 13 px, parfois en capitales avec espacement des lettres.

## Espacements et grille

- Conteneur principal : largeur max. **1440 px**, marge intérieure extérieure de 8 à 16 px.
- Sections : environ **100 px** d’espace vertical sur grand écran, **76 px** sur mobile.
- Grilles : 3 colonnes sur desktop, 2 sur tablette, 1 sur mobile ; gouttière de 14 à 20 px.
- Cartes : padding habituel **24 à 34 px** ; gaps intérieurs de 8, 12, 18 ou 24 px.
- Largeur de lecture des intros : environ **680 px** ; paragraphe du hero : environ **580 px**.

## Rayons, bordures et ombres

- Pills : `999px` (ou `border-radius: 999px`).
- Cartes : 24 à 28 px ; panneaux : 32 à 40 px.
- Bordures fines : noir à 5–10 % d’opacité ou blanc à 70–90 % d’opacité.
- Ombres larges et peu opaques : privilégier les ombres étalées et le reflet interne plutôt qu’un contour marqué.

## Composants et comportement

- Bouton principal : fond `--ink`, texte blanc, capsule, déplacement vertical léger au survol.
- Bouton secondaire : surface blanche, bordure légère, ombre douce.
- Cartes de service : icône sur carré arrondi, titre, description, badge de délai.
- Navigation flottante : capsule blanche translucide, `backdrop-filter: blur`, liens discrets ; menu mobile repliable.
- Respecter `prefers-reduced-motion`; privilégier de petites transitions et animations d’apparition non essentielles.
- Conserver un contraste lisible, des libellés accessibles et une hiérarchie sémantique des titres.

## Responsive

- Ruptures principales : **900 px** (grilles et navigation) et **620 px** (mise en page mobile).
- Sur mobile, empiler les colonnes, réduire les marges latérales et transformer les actions du hero en boutons pleine largeur.
- Éviter les largeurs fixes ; utiliser `clamp()` pour les grands titres et des grilles `minmax(0, 1fr)`.
