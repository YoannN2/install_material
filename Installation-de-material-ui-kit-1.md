# Installation de material-ui-kit-1.2.2 
* Material-ui est utilisé pour les projets vue * 
Dzipper le dossier material-kit-1.2.2 préalablement télécharger 

## Installation de l'envirronement 
 
### NodeJS 
Commencez par télécharger node.JS [ici](https://nodejs.org/en/) 
Le reste de la configuration ce passera en ligne de commande.  
 
### npm 
 
Une fois nodeJS installé, vous devez installer npm **NodePackageManager**. 
pour pouvoir installer le reste de la configuration.[docNPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) 
 
Copier coller ```npm install -g npm``` 
 
### vuejs 
 
Maintenant installer vueJS 2.x.x [docVue](https://vuejs.org/v2/guide/installation.html#NPM) 
 
Copier-coller ```npm install vue``` 
 
### VueCLI 
 
Une fois Vuejs installé vous aurez besoin de vueCLI [docVueCLI](https://cli.vuejs.org/guide/installation.html) 
VueCLI permet de creer votre proejt deja préconfiguré 

Copier-coller ```npm install -g @vue/cli```  
 
### SASS 
 
Vue material utilise le prépocesseur SASS, sans celui-ci rien ne fonctionenra. [docSASS](https://sass-lang.com/install)
 
Copier-coller ```npm install -g sass``` 
 
 
 
### Creation du projets 
 
Pour creer votre projet copier-coller ```vue create monprojet``` ** Les majuscules ne sont pas autorisé ** 
Ensuite vous aurez 3 choix dans la configuration
    *vue2.x
    *vue3.x
    *Manually
A vous de choisir celle qui convient le mieux. 
 
### Vue material 
 
Une fois l'installation terminé, rendez-vous dans votre dossier ```cd monprojet``` 

Ensuite copier-coller la commande ```npm install vue-material --save```[docMaterial](https://vuematerial.io/getting-started/) 

## Configuration customizer de material-kit 
 
#### Récuperer les fichiers minimum requis 
 
Maintenant pour faire fonctionner material vous aurez besoin de récuperer des dossiers/fichiers dans le dossier material-kit-1.2.2 Dzipper. 
 
Tout d'abord copier-coller le dossier assets(sans les images) dans le dossier src de votre projet. 
  
Ensuite copier-coller le dossier Plugins toujours dans le src de votre projet. 
 
On y reviendra par la suite. 
 
Maintenant vous aurez besoin de la liste des fichiers suivants qui se trouvent dans la racine du dossier material-kit-1.2.2 
    *.eslintrc.js
    *.jshintrc
    *postcss.config.js
    *API_Key 
**Copier-coller dans la racine de votre projet.** 
 

#### Font-Awesome 
 
Pour les icones il faudra importer font-awesome. [DocFontAwesome](https://fontawesome.com/how-to-use/on-the-web/referencing-icons/basic-use) 

Copier-coller dans la balise HEAD du fichier index.html qui se trouve dans le dossier Public de votre projet. 
 ```<!-- Fonts and icons -->   
    <link rel="stylesheet" type="text/css" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Roboto+Slab:400,700|Material+Icons" />
    <link rel="stylesheet" href="//fonts.googleapis.com/icon?family=Material+Icons">
    <link href="https://use.fontawesome.com/releases/v5.0.8/css/all.css" rel="stylesheet">
```
####Importer material ui 
 
Dans votre dossier projet copier-coller dans le fichier main.js 
    ```import MaterialKit from "./plugins/material-kit"; //npm install vue-material --save 
        import 'element-ui/lib/theme-chalk/index.css'; //npm install element-ui
        Vue.use(MaterialKit);
    ```

#### Installation des dépendances
**Toute les commandes suivantes doivent être fait dans votre dossier projet** 
 
Vous pouvez fermer le dossier material-kit nous n'en avons plus besoin, le reste ce passera dans votre dossier projet.
 
La derniere étapes consiste a isntaller diverses dépendances nécessaires aux modules importer dans les fichiers du dossier plugins. 

Pour utiliser : *```import { VPopover } from "v-tooltip";``` copier-coller ```npm install v-tooltip``` [tooltip](https://www.npmjs.com/package/v-tooltip) 
                *```import { Carousel, CarouselItem } from "element-ui";``` copier-coller ```npm install element-ui``` [elementUI](https://www.npmjs.com/package/element-ui) 
                *```import VueLazyload from "vue-lazyload";``` copier-coller ```npm install vue-lazyload``` [lazyload](https://www.npmjs.com/package/vue-lazyload) 
                *```import { directive as vClickOutside } from "vue-clickaway";``` copier-coller ```npm install --save click-away```  [ClickAway](https://www.npmjs.com/package/click-away) 

**DISCLAIMER** 
Ceci est une configuration qui permet d'utiliser tout ou parti des composants créer dans le dossier material-kit.Cette configuration est a modifier selon les cas.

### Problème

Si toutefois vous avez un problème lors du lancement de la commande ```npm run serve``` et qu'il vous manque des dépendances. 
Il vous faudra supprimé la partie tous ce qui conerne googleMap et mobileMenu dans le dossier plugins. 
*PS: il apparait dans plusieurs fichiers* 




