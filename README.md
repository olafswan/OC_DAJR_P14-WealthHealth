#### Projet 14 de la formation "Développeur d'application - JavaScript React" par OpenClassrooms

# Faites passer une librairie jQuery vers React

### Qu’allez-vous apprendre dans ce projet ?

Dans ce projet, vous participerez à la conversion d’une application de jQuery vers React 
pour une grande société financière.

Votre mission principale sera de refondre les pages clés de l’application en remplaçant 
un **plugin jQuery spécifique** par un **composant React**.
Cela impliquera une compréhension approfondie des deux technologies et leur interaction.

Vous serez chargé de mesurer les **performances** de l'application avant et après la conversion. 
Cette analyse de performance vous permettra de quantifier les avantages de la migration vers React.

La documentation du composant converti sera une étape importante de votre travail. Cela 
comprendra la rédaction de **documents techniques** détaillant l'architecture du composant, 
son fonctionnement, et les raisons de sa conception.

Vous livrerez les résultats de votre travail avec des rapports détaillés, y compris des 
analyses de performance et des explications sur les choix techniques effectués pendant la conversion.

### En quoi ces compétences seront-elles importantes pour votre carrière ? 
 
La migration d'une application de jQuery vers React est un exemple concret de la manière de 
réduire la dette technique et d'améliorer la performance d'une application web. 

La maîtrise de ces techniques est essentielle pour les développeurs front-end, surtout dans 
un contexte où la modernisation des applications existantes est souvent nécessaire. 

La capacité à documenter techniquement vos travaux est également essentielle pour la 
communication au sein des équipes de développement et pour assurer une maintenance efficace.

### Objectifs pédagogiques

* Analyser la performance d'une application web
* Déployer une application front-end
* Refondre une application pour réduire la dette technique
* Mettre en place son environnement Front-End
* Produire de la documentation technique pour une application

***
  
### Scénario :

Vous travaillez pour le département technologique d'une grande société financière, WealthHealth. 

![Logo de WealthHealth](https://user.oc-static.com/upload/2024/02/21/17085055322514_Capture%20d%E2%80%99e%CC%81cran%202024-02-21%20a%CC%80%2009.52.02.png)

Cette société utilise une application web interne, appelée HRnet, qui gère les dossiers des 
employés.

L'application est ancienne et utilise jQuery côté front end, ce qui entraîne des bugs 
considérables et une augmentation des plaintes en interne.

Votre équipe de développement s'efforce depuis un certain temps déjà de mettre à niveau 
l'application.  

Un matin, vous vous rendez au travail et remarquez les messages suivants de Jade, une collègue 
développeuse de l'équipe :

```bash
Jade :
Hello ! Tu as entendu la nouvelle ? La direction va ENFIN nous laisser mettre à jour HRnet et
le convertir en React ! Plus de maintenance du vieux code jQuery. Youhouuu !! 
Tu seras l'un des premiers développeurs à commencer à convertir le code ! 

Vous :
Super ! Dis m'en plus !

Jade : 
Les plus gros problèmes pour les utilisateurs de HRnet en ce moment sont les sélecteurs de date,
les fenêtres modales, les menus déroulants et les tableaux.
Nous avons reçu plusieurs plaintes disant que ces plugins jQuery sont très lents.  

Nous voulons donc créer nos propres composants React à la place de ces plugins jQuery tiers qui
sont utilisés dans l'interface utilisateur. Et on espère que la conversion de ces plugins jQuery
en composants React améliorera les performances et la stabilité.  

Vous :
Ok, compris.
Tous ces appels réseau et toute cette manipulation DOM nécessaire pour les plugins jQuery
s'additionnent et ralentissent les choses.
Et ce sera bien de commencer à avoir nos propres composants React pour avoir plus de contrôle sur
l'application. 

Jade :
Exactement ! La direction ne veut pas que cette première partie du processus de conversion prenne
trop de temps, alors s'il te plaît, choisis UN SEUL des quatre plugins jQuery et convertis-le en
composant React. (Je te les envoie plus tard dans la journée). Tu devras créer un repo GitHub
séparé pour le code converti. 

Vous :
Bien sûr ! C'est une bonne manière  d’avoir une version initiale de la nouvelle application plus
rapidement, et nous pourrons toujours itérer dessus plus tard.  

Jade :
Exactement ! Pour tester manuellement tes composants React convertis, tu devras aussi convertir
l'application HRnet principale en une application React. 
Comme tu sais que jQuery et React ne vont pas bien ensemble, nous voulons donc que la nouvelle
version de l'application soit 100% React et 0% jQuery.
Nous ne voulons pas créer un genre de monstre jQuery/React !  

Je t'enverrai le repo actuel de HRnet pour que tu puisses commencer. Nous aurons aussi besoin que
tu fasses des tests de performance et que tu nous fournisses des rapports.   

Vous :
Bien vu ! Je veillerai à inclure ces rapports de performance dans mes livrables. 

Jade :
Aussi, garde à l'esprit que nous voulons suivre un paradigme de programmation fonctionnel en
écrivant ces bibliothèques dans React, donc évite d'utiliser des classes quand tu le convertis.
Et essaie d’écrire des morceaux de code plus petits et modulaires et des fonctions autonomes pour
une modularité et une maintenabilité optimales.  

Aussi, assure-toi de documenter ton composant React converti avec une description générale de ce
que fait le composant et comment l'utiliser (un Readme) et des commentaires expliquant à quoi
chaque accessoire est destiné et comment il est utilisé. Le reste de l'équipe te remerciera ! 

Vous : D’accord, je m’occupe de ça ! 
```

Quelques minutes plus tard Jade vous envoie quelques détails supplémentaires :

```bash
Objet : récapitulatif des principales tâches WealthHealth
De : Jade
À : Moi

Voici un récapitulatif des principales tâches : 

Convertir l'ensemble du projet HRNet en React. 
Convertir l'un des quatre plugins jQuery actuels en React. Remplacer les 3 plugins jQuery
restants par des composants React que tu coderas toi-même, ou que tu peux importer depuis des
libraires existantes si tu manques de temps. 
Effectuer des tests de performance Lighthouse en comparant l'ancienne et la nouvelle application. 
Tu trouveras toutes les informations clés pour chaque tâche ci-dessous : 

Conversion du projet HRNet 

Voici le repo HRnet actuel. N'oublie pas que toute l'application HRNet doit être convertie en
React : 

Tu devras faire une nouvelle version des pages "Create Employee" et "Employee List" avec React.
Tu devras ajouter un système de gestion d'état (la version actuelle utilise un stockage local).
Tu dois aussi t'assurer que tout est cohérent au niveau du style. Pour cela, tu n'es pas obligé
de refaire le design de l'application, mais si tu veux changer le style pour quelque chose de
plus moderne, tu es le bienvenu.  
Si tu as le temps, tu peux tester le code React avec une suite de tests unitaires. Sinon, seuls
des tests manuels sont nécessaires. 
 
Conversion des plugins

Pour les plugins, n'hésite pas à consulter l'onglet Issues pour avoir plus de contexte sur les
problèmes que les utilisateurs rencontrent avec les plugins jQuery existants : issue sur les
sélecteurs de date, issues de fenêtres modales, issue sur menus déroulants, et issue sur les
tableaux. 

Voici la liste des plugins jQuery actuellement utilisés qui doivent être convertis : 

Plugin de sélection de date
Plugin de fenêtre modale - jQuery.modal.js
Menus déroulants
Plugin pour les tables de données
De plus, lors de la conversion d'un plugin jQuery en un composant React, il faut garder à
l'esprit de ne convertir que le code qui traite de la fonctionnalité réelle de l'interface
utilisateur du plugin. Par exemple, si un plugin jQuery inclut du code AJAX, tu n’as pas besoin
de le convertir. Si tu convertis un plugin jQuery pour une fenêtre modale, concentre-toi sur la
création d'un composant React qui fonctionne comme une fenêtre modale, et rien d'autre.

Tests de performance

Nous voulons également mesurer des données quantifiables (ex. : temps de chargement des pages,
appels réseau) pour nous assurer que la conversion de l'application à React améliore effectivement les performances. Pour cela, fais bien des audits de performance Lighthouse.
Pour comparer, tu devras en faire un pour l'application jQuery HRnet actuelle, puis un autre
une fois que l'application et le plugin jQuery choisi seront convertis en React.

Penses bien à faire un build de l'application avant de faire ton audit. Ça impactera grandement
les performances de ton application.

C'est tout ! Une fois que l'application HRnet en React fonctionne, tu peux publier le composant
React sur npm sous forme de package et partager le lien pour que nous puissions l'utiliser si
nécessaire. Si tu as du mal avec npm, tu peux utiliser les paquets GitHub comme alternative.

Aussi, fais-moi savoir quand tout est fait et nous ferons une révision du code pour répondre aux
commentaires restants.

J'ai hâte de voir ce que tu vas faire ! 

Jade
```

### Pièces jointes :

[Repo HRnet](https://github.com/OpenClassrooms-Student-Center/P12_Front-end)

[issue sur les sélecteurs de date](https://github.com/OpenClassrooms-Student-Center/P12_Front-end/issues/1)

[issues de fenêtres modales](https://github.com/OpenClassrooms-Student-Center/P12_Front-end/issues/3)

[issue sur menus déroulants](https://github.com/OpenClassrooms-Student-Center/P12_Front-end/issues/4)

[issue sur les tableaux](https://github.com/OpenClassrooms-Student-Center/P12_Front-end/issues/2)

[Plugin de sélection de date](https://github.com/xdan/datetimepicker)

[Plugin de fenêtre modale - jQuery.modal.js](https://github.com/kylefox/jquery-modal)

[Menus déroulants](https://github.com/jquery/jquery-ui/blob/master/ui/widgets/selectmenu.js)

[Plugin pour les tables de données](https://github.com/DataTables/DataTables)

Ça y est, vous avez toutes les informations dont vous avez besoin. Maintenant, le plus dur sera de choisir quel plugin jQuery convertir !

***

### Livrables :
1. Un fichier au format TXT ou PDF contenant les liens vers :
   - votre code source sur GitHub de la bibliothèque ReactJS converti depuis le plugin jQuery
sélectionné (un seul plugin doit être converti) ;
   - votre projet complet sur GitHub ;
   - la bibliothèque React convertie publiée sur npm (ou GitHub Packages) ;
2. Un rapport de performance LightHouse au format PDF de HRnet fonctionnant avant et après la
conversion de la bibliothèque. 

### Cours :
[Écrivez la documentation technique de votre projet](https://openclassrooms.com/fr/courses/6398056-ecrivez-la-documentation-technique-de-votre-projet)

### Ressources :
[Lighthouse - Tools for Developers](https://developers.google.com/web/tools/lighthouse/)

[Creating a Library of React Components using Create React App](https://hackernoon.com/creating-a-library-of-react-components-using-create-react-app-without-ejecting-d182df690c6b)


### Résultat final lors du passage de la soutenance :
[Lien du site](www.google.com)
