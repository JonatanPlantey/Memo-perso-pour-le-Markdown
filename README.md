
<h1 align="center">Mémo personnel pour l'usage du Markdown sur GitHub/GitLab</h1>

<p align="center">

<em>L'extension</em> <strong>.md</strong> <i>provient de</i> <b><i>Markdown</i></b>

[![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](https://github.com)
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Open Source? Yes!](https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github)](https://github.com/Naereen/badges/)
[![Awesome Badges](https://img.shields.io/badge/badges-awesome-green.svg)](https://github.com/Naereen/badges)

</p>

## Possibilités de présentation du texte en Markdown pour Github[^Impossibilités]
*Complétées par certaines possibilités très utiles permises par le langage HTML.*

Le plus souvent, les possibilités recensées ci-dessous sont celles utilisées dans ce fichier dans leur ordre d'utilisation.
Si certaines possibilités, affichées dans le navigateur ne sont pas explicitées, elles pourront être retrouvées facilement en éditant ce fichier README dans un éditeur de texte.

<hr>

## 1. Retour ligne et élément de rupture horizontale

    Selon l'emplacement des besoins, derrière des tags (ou balise) demandant un
    affichage spécifique ou non, les retours lignes affichés coïncident avec les
    retours lignes tapés dans l'éditeur de texte ou doivent être forcés en finissant
    le texte par un deuxième retour ligne ou encore par le tag <br/>.
    Un élément de rupture horizontale (ligne grise épaisse séparant deux parties)
    peut être ajouté par le tag <hr>.

<hr>

## 2. Afficher du texte tel qu'il est édité (sans interprétation dans l'affichage)

### a. Après une ligne vide, commencer une ligne par 4 espaces permet d'afficher grisé, dans tout navigateur, le texte qui a été tapé dans l'éditeur de texte sans aucune interprétation en langage Markdown.

Voici un text précédé par une ligne vide et 4 espaces (les tags entourant le texte permettent d'afficher le texte en italique mais ne sont pas interprétés)

<b>Code</b>

    <i>Exemple</i>

Pour le même texte précédé par une ligne vide mais sans les 4 espaces, les tags ont été interprétés et le texte s'affiche en italique.

<b>Rendu</b>

<i>Exemple</i>
<br/>

### b. Utilisation d'un autre tag en langage HTML, pour par exemple bloquer le code Markdown affichant une image, en vue de le présenter ci-dessous.

<b>Code avec blocage de l'exécution de code (bloqué par les tags à la 1ère et 3ème ligne)</b>

    <pre>
    ![Caption](https://upload.wikimedia.org/wikipedia/commons/8/85/Stereographic_projection_in_3D.png)
    </pre>

<b>Rendu sans le blocage de l'exécution de code</b>

![Caption](https://upload.wikimedia.org/wikipedia/commons/8/85/Stereographic_projection_in_3D.png)
<br/>

<hr>

## 3. Afficher du code

### a. Pour afficher du code, et peut-être éviter de l'exécuter, on l'entoure d'accents graves.

<b>Code</b>

    `le code entre accents graves est grisé`

<b>Rendu</b>

`le code entre accents graves est grisé`
<br/>

### b. Le code écrit à l'intérieur d'une paire de trois accents graves se grise et se colore parfois s'il est reconnu (voir ci-dessous le code au format json).

<b>Code</b>

    ```json
    {
      "Nom de Famille": "Plantey",
      "Prénom": "Jonatan",
      "age": 43
    }
    ```

<b>Rendu</b>

```json
{
  "Nom de Famille": "Plantey",
  "Prénom": "Jonatan",
  "age": 43
}
```
<br/>

<hr>

## 4. Afficher un tableau

### Le texte écrit dans un tableau peut au choix, dans chaque colonne, être aligné à gauche, centré, ou aligné à droite.
On notera qu'une ligne sur deux est grisée sur GitHub (et non sur GitLab) pour faciliter la lecture.

<b>Code</b>

```
|Texte aligné à gauche|Texte centré|Texte aligné à droite|
|:-|:-:|-:|
|1ère ligne|1ère ligne|1ère ligne|
|2ème ligne|2ème ligne|2ème ligne|
|3ème ligne|3ème ligne|3ème ligne|
|Dernière ligne|Dernière ligne|Dernière ligne|
```
<b>Rendu</b>

|Texte aligné à gauche|Texte centré|Texte aligné à droite|
|:-|:-:|-:|
|1ère ligne|1ère ligne|1ère ligne|
|2ème ligne|2ème ligne|2ème ligne|
|Dernière ligne|Dernière ligne|Dernière ligne|
<br/>

<hr>

## 5. Ajuster la taille du texte
Les tailles varient du plus grand au plus petit en ajoutant les tags Markdown consignés dans le tableau ci-dessous.
On y ajoute les tags HTML compatibles dans la visualisation sous Github. On notera que seuls les tags en HTML fonctionnent à l'intérieur des tableaux :

<b>Code et rendu</b>

| Code en Markdown | Code en HTML | Rendu |
|:-:|:-:|:-:|
|# Taille 1|`<h1>Taille 1</h1>`|<h1>Taille 1</h1>|
|## Taille 2|`<h2>Taille 2</h1>`|<h2>Taille 2</h2>|
|### Taille 3|`<h3>Taille 1</h3>`|<h3>Taille 3</h3>|
|#### Taille 4|`<h4>Taille 4</h4>`|<h4>Taille 4</h4>|
|##### Taille 5|`<h5>Taille 5</h5>`|<h5>Taille 5</h5>|
|###### Taille 6|`<h6>Taille 6</h6>`|<h6>Taille 6</h6>|
<br/>

<hr>

## 6. Afficher du texte en italique, en gras, en gras et italique ou barré.
On notera ci-dessous les différentes possibilités offertes par le langage HTML, et notamment la possibilité de composer avec plusieurs tags.

<b>Code et rendu</b>

| Code en Markdown | Code en HTML | Rendu |
|:-:|:-:|:-:|
|`Texte normal`|`Texte normal`|Texte normal|
|`*Texte en italique*`|`<i>Texte en italique</i>`|<i>Texte en italique</i>|
| |`<em>Texte en italique</em>`|<em>Texte en italique</em>|
|`**Texte en gras markdown**`| |**Texte en gras markdown**|
||`<strong>Texte en gras HTML</strong>`|<strong>Texte en gras HTML</strong>|
| |`<b>Texte en gras HTML</b>`|<b>Texte en gras HTML</b>|
||`<strong><i>Texte en gras et italique HTML</i></strong>`|<strong><i>Texte en gras et italique HTML</i></strong>|
||`<b><i>Texte en gras et italique HTML</i></b>`|<b><i>Texte en gras et italique HTML</i></b>|
|`~Texte barré~`|`<strike>Texte barré<strike>`|<strike>Texte barré</strike>|
||`<strike><b><i>Texte gras, italique et barré HTML</i></b></strike>`|<strike><b><i>Texte gras, italique et barré HTML</i></b></strike>|
<br/>

<hr>

## 7. Afficher un lien, une image, et une image renvoyant vers un lien.
On notera ci-dessous les différentes possibilités offertes par le langage HTML, et notamment la possibilité de composer avec plusieurs tags

<b>Code pour afficher un lien</b>

<pre>[Lien vers wikipédia](https://fr.wikipedia.org)</pre>

<b>Rendu</b>

[Lien vers wikipédia](https://fr.wikipedia.org)
<br/>

<b>Code pour afficher une image (autre que celui présenté plus haut)</b>

Noter l'ajout de width="400" (largeur = 400 pixels) à l'URL permettant de redimensionner la taille de l'image et l'ajout des tags pour centrer l'affichage.

    <p align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/f6/Riemann_sphere.png" width="400">
    </p>

<b>Rendu</b>

<p align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/f/f6/Riemann_sphere.png" width="400" align="center">

</p>
<br/>

<b>Code pour afficher une image cliquable renvoyant vers une autre page (image + lien)</b>

<pre>[![Caption](https://upload.wikimedia.org/wikipedia/commons/d/d1/Wikipedia-logo-v2-fr.svg)](https://fr.wikipedia.org)</pre>

<b>Rendu</b>

[![Caption](https://upload.wikimedia.org/wikipedia/commons/d/d1/Wikipedia-logo-v2-fr.svg)](https://fr.wikipedia.org)
<br/>

<hr>

## 8. Début de ligne : puces, numérotation et présentation pour une citation de texte.
En début de lignes, on obtient les puces usuelles grâce au symbole *.<br/>
Les numérotations s'obtiennent quant à elles naturellement.

<b>Code pour afficher les puces</b>

    * Item 1
     
    * Item 2	

<b>Rendu</b>

* Item 1

* Item 2
<br/>

<b>Code pour afficher les puces</b>

    1. Item a
     
    2. Item b	

<b>Rendu</b>

1. Item a 
 
2. Item b
<br/>

<b>Code pour afficher une barre verticale et présenter par exemple une citation</b>

    > Maître Corbeau, sur un arbre perché,<br/>
    Tenait en son bec un fromage.<br/>
    Lui tint à peu près ce langage :<br/>
    Et bonjour, Monsieur du Corbeau.<br/>
    Que vous êtes joli ! que vous me semblez beau !

<b>Rendu</b>

> Maître Corbeau, sur un arbre perché,<br/>
Tenait en son bec un fromage.<br/>
Lui tint à peu près ce langage :<br/>
Et bonjour, Monsieur du Corbeau.<br/>
Que vous êtes joli ! que vous me semblez beau !
<br/>

<hr>

## 9. Notes de bas de page
Pour coder une note en bas de page, il est possible d'utiliser une numérotation ou de façon plus explicite un balisage contenant des mots sans espace comme dans l'exemple ci-dessous.

<b>Code</b>

    Cette année-là[^Année_de_ma_naissance], je n'avais pas encore un an.

<b>Rendu</b>

Cette année-là[^Année_de_ma_naissance], je n'avais pas encore un an.
<br/>

<hr>


[^Impossibilités]:*Sur GitHub/GitLab* ***il n'est pas possible*** *d'utiliser le langage Markdown pour* ***souligner*** *ou* ***mettre en couleur*** *du texte.*

[^Année_de_ma_naissance]: 1979
