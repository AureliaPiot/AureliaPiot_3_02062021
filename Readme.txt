GUIDE

rangement des élements scss dans des differents fichiers suivant la methode 7-1
dans le dossier Sass/ ,il s'y trouve :
.abstract/
-> variables_mixins.scss
contient toutes les variables et mixins dans un même fichier.

.Base/
-> reset.scss
contient toute les balises classes génerique

.Components/
-> Loader.scss
le loader qui a été isoler dans un fichiers

.Layout/
->Header_Footer.scss
->fonctionnement.scss
->locate.scss
->reservation.scss
->restaurant.scss

"header_Footer.scss" est le seul fichier commun à la page d'accueil et aux pages restaurant,
tous les autres sont des parties de la pages d'accueil 

.Pages/
->restaurants_pages.scss
tout les éléments qui forment les pages restaurant sont dans le même fichiers, il y à trop peu d'éléments pour les separés.(simple preference)


->main.scss
->page.scss
contient les @imports nécessaire à chaque page

->main.css.map
->page.css.map
fait le lien entre les fichiers scss et les fichiers css selon le Package.json
pas present sur le Github mais se créer automatiquement apres une commande Script.
_____________________________________________

-Le W3C peux renvoyer des avertissments concernant certaint prefix.avertissement qui previent l'utilisation de fonction propre à certains navigateurs, ce qui est normal.

-Remplacement de "Background-clip:text" par "b "Background-clip:content-box" car la valeur text n'est pas valide sur W3C, mais ne derange pas avec les prefix "-webkit" et "moz".
ce qui donne :
            background-clip: content-box;
            -webkit-background-clip: text;
            -moz-background-clip: text;
"content-box" car ont a besoin d'une valeur de base.            

- le fichier css appliqué est celui qui a été prefixier avec les commande " npm run prefix" pour le "style.css et "npm run prefix_page" pour le "style_page.css .

- chaques éléments scss à sa parties mediaQuery integrer (et ne sont donc pas tous rassembler au même endroit)  

-les fichiers Sass sont disponibles sur le github 
-le fichier package.json est disponibles sur le github 
-deux type de scripts sont présents, un pour chaques pages et un pour leurs appliqués les prefixes .

___
-les dimensions sur la page des plats des restaurant est pensé pour que le plat reste entierment lisible sur les differents affichages.

