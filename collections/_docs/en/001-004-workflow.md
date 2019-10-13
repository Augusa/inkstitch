---
title: "Organisation du travail"
permalink: /docs/workflow/
excerpt: ""
last_modified_at: 2019-10-13
toc: true
---
![Ink/Stitch workflow](/assets/images/docs/en/workflow-chart.svg)

## ![Create Icon](/assets/images/docs/workflow-icon-create.png) Etape 1: Créer une image vectorielle
Au début, vous avez besoin d’une idée ou d’une image à transférer dans un fichier de broderie. Vous pouvez le peindre à partir de zéro ou utiliser une image existante.

### Dessiner avec Inkscape

#### Créer des chemins

Inkscape offre des outils variés pour créer des images vectorielles. Vous pouvez, par exemple, utiliser  
* ![dessiner des lignes à main levée](/assets/images/docs/inkscape-tools-freehand.png) dessiner des lignes à main levée (<key>P</key>)
* ![freehand lines icon](/assets/images/docs/inkscape-tools-bezier.png) Courbes de Bézier (<key>B</key>)

Essayer aussi d'autres outils de la barre des outils. Par exemple des formes spécifiques comme 

* ![Carré icon](/assets/images/docs/inkscape-tools-square.png) Rectangle
* ![cercle icon](/assets/images/docs/inkscape-tools-circle.png) Cercle
* ![polygone icon](/assets/images/docs/inkscape-tools-polygon.png) Etoile/Polygone
* ![spirale icon](/assets/images/docs/inkscape-tools-spiral.png) Spirale

#### Modifier les chemins

Modifier les objets et les chemins avec:
* ![outil de sélection icon](/assets/images/docs/inkscape-tools-select.png) Outil de sélection (<key>S</key>) et 
* ![outil noeud icon](/assets/images/docs/inkscape-tools-node.png) Outil d'édition de noeuds (<key>N</key>)

Mettez à l'échelle, faites pivoter et déplacez tout l'objet avec l'outil de sélection. L'éditeur de nœuds sert à manipuler les nœuds sélectionnés, etc.
De plus, vous pouvez utiliser les effets de chemin (`Chemin> Effets de chemin ... '). N'oubliez pas de toujours reconvertir l'objet résultant en un chemin, comme décrit ci-dessus.


### Utiliser une image / un graphique existant

Lorsque vous basez un dessin sur une image ou un graphique existant, chargez-le dans Inkscape dans son propre calque. Certains graphiques sont compatibles avec Inkscape [fonction de traçage automatique](https://inkscape.org/fr/doc/tutorials/tracing/tutorial-tracing.html) (`Chemin > Vectoriser une image matricielle` ou `Shift+Alt+B`), surtout si vous simplifiez d’abord l’image dans un éditeur graphique (par exemple avec[GIMP](https://www.gimp.org/)).

**Astuce:** Si vous avez Linux et avez besoin de vectoriser un trait, vous pouvez utiliser un autre plugin Inkscape, qui a pour but de faire [traçage du trait d'axe](https://github.com/fablabnbg/inkscape-centerline-trace). For embroidery purposes it might only apply to simple shapes.
{: .notice--info }

Après le traçage, nettoyez les formes vectorielles en utilisant `Chemin> Simplifier` (` Ctrl + L`) et en supprimant les nœuds à la main lorsque cela est possible. Le but est d’utiliser le moins de courbes de Bézier possible pour représenter l’image.

Lorsque l’image doit être tracée à la main, utilisez l’outil de dessin à main levée. Cet outil crée des chemins avec beaucoup de noeuds de Beziér, simplifiez donc autant que possible les courbes.

**Astuce:** Travailler avec une image SVG existante peut vous faire gagner beaucoup de temps. Songez donc à utiliser votre moteur de recherche avec le filtre de recherche d'image défini sur SVG.
{: .notice--info }

### Texte

Pour le texte, choisissez une police avec soin. Il est assez difficile de faire en sorte que le satin soit beau quand il fait 1mm de large ou moins. Les polices sans empattement ont tendance à être les plus faciles. Pour un texte de moins de 4 mm de hauteur, il vous sera très difficile de donner une belle apparence aux lettres minuscules. Par conséquent, considérez les majuscules. Les polices Cursive / Script peuvent bien fonctionner, mais ce ne sera pas aussi facile que vous le pensez.

## ![Vectorize](/assets/images/docs/workflow-icon-vectorize.png) Etape 2: Convertir en vecteur de broderie et paramétrer

À ce stade, vous aurez une représentation graphique vectorielle de votre image. La prochaine chose à faire est de convertir vos vecteurs en un type compris par Ink / Stitch.

### Le dialogue Objets

Nous vous recommandons de faire un usage intensif des calques et des groupes à ce stade.

Dans le panneau des objets (ouvert avec <key>Ctrl</key><key>Shift</key><key>O</key>, vous pouvez gérer des calques, des groupes et des objets.
Vous pouvez enregistrer l'image d'origine en dupliquant le calque:

* Faites un clic droit sur le calque (si vous n'avez pas renommé le calque, il s'appellera `Calque 1`)
* Cliquez sur `Dupliquer`
* Fermez l'oeil en cliquant dessus.

Cela rendra le premier calque invisible. Tout calque, groupe ou forme vectorielle défini comme invisible sera ignoré par Ink/ Stitch. Nous allons maintenant travailler avec la copie.
![Dialogue objet](/assets/images/docs/en/objects-panel.png)

### Groupes

Utilisez des groupes pour structurer votre document:

* Sélectionnez des objets avec votre souris
* Ajouter ou supprimer des objets avec <key>shift</key><key>click</key>
* Appuyez sur <key>Ctrl</key><key>G</key>

Grouper des objets fonctionne comme suit:
*Sélectionnez le(s) groupe(s)
* Appuyez sur <key>Ctrl</key><key>Shift</key><key>G</key>

### Convertir en chemin

Transformez ** tous les objets ** que vous souhaitez broder en chemins:

* Sélectionner tous les objets (`Ctrl+A`)
* Cliquer sur ![convertir en chemin](/assets/images/docs/inkscape-tools-convert-to-path.png) ou appuyer <key>Ctrl</key><key>Alt</key><key>C</key>.

**Info:**Les objets qui ne sont pas de type "chemin" sont ignorés par Ink/Stitch.
{: .notice--warning }

### Types de point

Ink/Stitch propose différents types de points. Selon le type de point que vous souhaitez utiliser, vous devez définir la couleur de remplissage ou les paramètres de trait avec`Objet > Fond et forme...` (<key>Ctrl</key><key>Shift</key><key>F</key>).

Regardez ce tableau et suivez les liens pour comprendre comment créer un type de point spécifique:

Objet chemin | Type de point
---|---|---
Trait(pointillé) |[point droit](/docs/stitches/running-stitch/), [point manuel](/docs/stitches/manual-stitch/), [point zig-zag](/docs/stitches/zigzag-stitch/), [point triple](/docs/stitches/bean-stitch/)
Deux traits combinés (avec échelons optionnels) | [colonne satin](/docs/stitches/satin-column), [e-stitch](/docs/stitches/e-stitch)
Closed path with a fill color | [fill stitch](/docs/stitches/fill-stitch/)
{: .equal-tables }

### Parametrize

Set parameters using `Extensions > Ink/Stitch  > Params`. You find a description for each parameter in the [Params](/docs/params/) section of this documentation. Each time you change parameter values, you'll be able to see the simulated result in a preview window. Once you are satisfied with the result, click `Apply and close` to save the values into your SVG-file.

At this point, save your SVG file. If Inkscape is starting to become sluggish (due to an Inkscape memory leak), restart it before continuing.


## ![Create Icon](/assets/images/docs/workflow-icon-order.png) Step 3: Plan Stitch Order & Attach Commands

### Stitch Order

When you're designing for embroidery machines that can't cut the thread mid-sew or switch colors automatically, you're going to want to optimize your stitch path to reduce or hide jump stitches and make minimal color changes. Also try to avoid stitching over jump stitches when possible, because it's a total pain to trim them by hand when you do.

The order of stitching also affects how the fabric pulls and pushes. Each stitch will distort the fabric, and you'll need to take this into account and compensate accordingly. [More Information](/tutorials/push-pull-compensation/)

Once you've created all vectors, it's time to put everything in the right order. This is where the Inkscapes Objects tool (`Objects > Objects ...`) comes in useful. Optimize your order to minimize color changes and reduce or hide jump-stitches.

Ink/Stitch will stitch objects in exactly the order they appear in your SVG document, from lowest to highest in stacking order. If the distance between two objects is long, Ink/Stitch will add a jump-stitch between them automatically. It uses the color of the object to determine thread color, so changes in color from one object to the next will result in a thread-change instruction being added to the embroidery output file.

**Tip:** Inkscape gives you the ability to "raise" and "lower" objects in the stacking order using the PageUp and PageDown keys. The new functions "Stack Up" and "Stack Down" will give you much better control over the stacking order. So we recommend to rather bind PageUp and Page Down to them. [More Information](/docs/customize/#shortcut-keys)
{: .notice--info }

**Info:** You can also manually manipulate the underlying SVG XML structure by using Inkscape's XML Editor pane (`CTRL-SHIFT-X`). Its "Raise" and "Lower" buttons directly manipulate the order of XML tags in the SVG file and are not subject to the same limitations as the original PageUp and PageDown. Note that the ordering of XML tags in the XML Editor tool is the _reverse_ of the order of objects in the Objects tool.
{: .notice--info }

### Commands

[Commands](/docs/commands/) also help to optimize your stitch path. You can set start and ending points, push the frame into defined positions or set trim and cut commands, etc.

## ![Create Icon](/assets/images/docs/workflow-icon-visualize.png)  Step 4: Visualize

Ink/Stitch supports three ways to preview your design:

* [Simulator](/docs/simulate/)
* [Print Preview](/docs/print/)
* [Display Stitch Plan](/docs/import-export/#method-2-display-stitch-plan) (Undo with <key>Ctrl</key><key>Z</key>)

## ![Create Icon](/assets/images/docs/workflow-icon-export.png) Step 5: Save the Embroidery File

Once you've got everything in the right order, run `File > Save as...` to [export](/docs/import-export/) to a file format supported by your machine. Most machines can support DST, and some Brother machines prefer PES. Do not forget to also save your file in the SVG-format. Otherwise it's going to be difficult to change details later.

## ![Create Icon](/assets/images/docs/workflow-icon-testsew.png) Step 7: Test-sew

There's always room for improvement! To test out your design, prepare a test piece of fabric that matches your final fabric as closely as possible. Use the same stabilizer and the exact same fabric if possible. For t-shirts, try to find a similar fabric (usually knit). Knits need a lot of stabilization.

Sew out the design, watching the machine to make sure that there aren't any surprises. Watch out for gaps that indicate that the fabric has been distorted. Also search for areas where stitches are piling up too closely and the machine is having trouble sewing, which indicates that the stitch density is too high.

## ![Create Icon](/assets/images/docs/workflow-icon-optimize.png) Step 8+: Optimize

Then go back and tweak your design. Hopefully it only takes a few tries to get it how you want it. Once you're done, copy the final embroidery file from your output directory, just to avoid accidentally overwriting it in the future.

