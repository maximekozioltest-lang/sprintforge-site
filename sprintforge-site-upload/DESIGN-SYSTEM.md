# ClozingSystem · Direction visuelle de la landing page

La landing page conserve la structure générale du site de départ, avec une identité adaptée à ClozingSystem. Références : le site ClozingSystem et la présentation de marque fournie par Maxime.

## Identité

- **Ambiance :** directe, affirmée et haut de gamme ; bleu nuit, crème et rouge, avec un accent or.
- **Formes :** grandes capsules pour les boutons et badges, cartes très arrondies (24 à 40 px), bordures discrètes.
- **Profondeur :** ombres diffuses, reflets blancs internes, fonds translucides avec flou pour la navigation.

## Couleurs

| Rôle | Valeur | Usage |
| --- | --- | --- |
| Fond global | `#F6F3ED` | Fond de page crème |
| Surface sombre | `#10243E` | Hero et panneaux principaux |
| Surface chaude | `#FFFFFF` | Cartes et zones de lecture |
| Blanc | `#FFFFFF` | Cartes et champs |
| Encre | `#101B2D` | Boutons et panneaux sombres |
| Titres | `#101B2D` | Titres sur fond clair |
| Texte secondaire | `#536174` | Paragraphes et navigation |
| Texte discret | `#748092` | Métadonnées, légendes |
| Accent | `#ED3025` | Logo, liens, icônes et repères |
| Accent lumineux | `#FF5144` | Dégradés et accent sur fond sombre |
| Or | `#F2C450` | Accent du titre principal |

Variables disponibles dans `src/styles/global.css` : `--bg`, `--surface`, `--paper`, `--ink`, `--heading`, `--muted`, `--quiet`, `--accent` et `--accent-light`.

## Typographie

- **DM Sans** pour l’interface et les paragraphes.
- **Archivo Black** pour le titre principal et les accents de marque.
- **IBM Plex Mono** pour les repères courts et les libellés techniques.
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

## Marque et contenu

- Le nom affiché est **ClozingSystem** ; le pictogramme est un C rouge sur fond bleu nuit.
- Ton : direct, sans promesse chiffrée inventée ni faux témoignage, client ou coordonnées.
- Axe : sortir des formations de vente standards, travailler mental et technique sur le terrain, concentrer l’effort sur les profils à fort potentiel de progression.

## Responsive

- Ruptures principales : **900 px** (grilles et navigation) et **620 px** (mise en page mobile).
- Sur mobile, empiler les colonnes, réduire les marges latérales et transformer les actions du hero en boutons pleine largeur.
- Éviter les largeurs fixes ; utiliser `clamp()` pour les grands titres et des grilles `minmax(0, 1fr)`.
