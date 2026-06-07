



Telechargons le Unity Hub pour pas ce casser la tete sur l install
![alt text](image-1.png)
https://docs.unity.com/en-us/hub


Allons cherchez la version de la formation   
![alt text](image.png)   
https://unity.com/releases/editor/whats-new/6000.3.13f1   


Allons dans install
Et ajoutons avec le manager a droite sur limage:
= Android Build Support
  - OpenJDK
  - Android SDK / NDK
![alt text](image-2.png)


Il nous faut aussi le IL2CPP pour Meta et pour faire des codes utilisants le Job System pour loptimisation
![alt text](image-3.png)

Creeons un project
![alt text](image-4.png)

Il y a des templates de projet configurer pouar la XR ou la VR.
![alt text](image-5.png)

Nous on va partir de rien pour apprendre a setup le projet sans outils en trop.
Avec un URP Render Piple blank project
![alt text](image-6.png)

Cest outils seront installer
![alt text](image-7.png)


On veut pas donner notre code a Unity.
Creeons un projet Local
![alt text](image-8.png)


Unity U/Q:  
![alt text](image-9.png)

Creons un projet sur Github que je vais appeler HelloUnityA4

![alt text](image-11.png)


Allons sauver notre projet avec GitHub... Vu que Unity me laisse pas faire

![alt text](image-14.png)
![alt text](image-12.png)
![alt text](image-13.png)
![alt text](image-19.png)
![alt text](image-15.png)



`2026_06_06_unity_hello_unity_a4`

![alt text](image-17.png)




Bon bah on peu aller creer un jeu en godot pendant que Unity charge:   
![alt text](image-18.png)


Pendant que ca charge on peut aller verifier que votre projet c est bien creer

![alt text](image-20.png)



Vous povuez meme prendre le temps de vous creer un repistory en votre nom pour votre page d acceuile
[![alt text](image-21.png)](https://github.com/EloiStree
)



Nous voila en Unity3D

Verifions que on a un gitignore
![alt text](image-22.png)



Petit add commit pull push

Verifions que lon voit les extensions de fichier et les fichiers cacher.
![alt text](image-23.png)



`git status`
 pour verifier qu il y bien un git ignore et pas de fichier temporaire
`git add .`
![alt text](image-24.png)


Un petit commit.
`git commit -m "Empty ready project"`

Un petit pull push pour le sauver en ligne.
Si on fait de la merde



Alors vu que Unity n a aps creer un read me en ligne et creer le projet local il faut le push sur le stream our le force push . C est pas necessairement la meilleur maniere.
`Force Push` 
![alt text](image-25.png)


Essayons de retirer les packages qui serve t a rien
![alt text](image-26.png)


Disable AI
![alt text](image-27.png)

Disable Cloth 
![alt text](image-28.png)


Un a un ca fait long allons dans manifest.json
![alt text](image-29.png)



Evidement ca peut etre dangereux de retirer des modules
Mais ai je besoin de ca dans mon projet...  
```
    "com.unity.modules.physics2d": "1.0.0",
    "com.unity.modules.terrain": "1.0.0",
    "com.unity.modules.terrainphysics": "1.0.0",
    "com.unity.modules.wind": "1.0.0",
    "com.unity.ai.navigation": "2.0.12",
```
![alt text](image-30.png)



Un petit Add commit pull push si vous avez pas tous caser

![alt text](image-31.png)


Allons sur l asset store de Unity
![alt text](image-32.png)


Et cherchons le Meta XR SDK
(Ca change toujours de nom tout les ans, taper oculus meta xr)
![alt text](image-33.png)
https://assetstore.unity.com/packages/sdk/meta-xr-sdk-9022845


Ajoutons les packages a notre projet ouvert.
![alt text](image-34.png)


Quand vous fait un tutorial en ligne regarder bien la version utiliser et les numeros d os du quest ( si il est bien ajour)

![alt text](image-35.png)


Clicker installer et aller boire un cafe 😉
Ou faire un jeu sur Scratch   
https://scratch.mit.edu/  

![alt text](image-36.png)
![alt text](image-37.png)



Je vous laisse choisir si vous voulez partager avec Meta
![alt text](image-38.png)


Je vais skip en fermant la fenetre
![alt text](image-39.png)


On peut aller sur le menu mais comme il nous le propose
![alt text](image-40.png)
![alt text](image-41.png)


Avant de fix les problemes, il nous faut installer open xr
![alt text](image-42.png)
![alt text](image-43.png)


Je suppose que oui du coup.
![alt text](image-44.png)

Fixons  ce que Unity XR Plug in nous propose.
![alt text](image-45.png)
![alt text](image-46.png)


Ca ma telecharger une XR Simulator
![alt text](image-47.png)

Mais je l utilise peu a mon niveau.

J ai tendance a creer mes outils hors de la VR et de le tester en VR quand l outil est pret.
Ce qui fait que je peux me passer du simulateur.  


Ok, validateur est bon. Allons faire un add commit pull push.
![alt text](image-48.png)



Allons setup les paramettres du projet
![alt text](image-50.png)

Et validons ce qu il nou reste a valider.
![alt text](image-51.png)

Parlans de cela est pas encore sur Android mais sur Window
![alt text](image-53.png)
![alt text](image-54.png)

Bon.. bah du coup allons mettre notre projet en Android


And Build profiles
![alt text](image-55.png)

![alt text](image-56.png)


Coffee time
![alt text](image-57.png)


Changer pour android peu changer des paremetres.
Refait un tour dans le precedent menu.
![alt text](image-58.png)

Prenons la dernier version de C#
![alt text](image-59.png)



Si vous utilisez des servers externes local ou des AI dans votre jeux: (example LLM Studio of Flask Python)
![alt text](image-60.png)

Si votre application doit aller dans le fichier du Quest pour chercher des images, video ou avoir un dossier dans l racine de la carte sd pour etre plus facilement trouvable par lutilisateur
![alt text](image-61.png)


Be sure to use a unique namepackage for your apk
pay.company.appuniquename.
⚠ ALphaNumericm pas d'espsace ou de character speciaux ⚠
![alt text](image-63.png)


--------

Creeons une scene vide
![alt text](image-49.png)

Puis ajoutons la au prochain build
![alt text](image-64.png)



Retirer la camera et allons dire bonjour au Block de Meta
![alt text](image-65.png)

All the blocks
![alt text](image-66.png)

Ajoutons une camera
![alt text](image-67.png)

Cela nous ajoute les Composants tout chaud .
AJoutons y un sphere dans chaque mains pour les voir avec un ou deux centimetres
![alt text](image-68.png)


On veut faire de la realiter augmenter avec l passthrouhg
![alt text](image-69.png)

On veut voir les manettes
![alt text](image-70.png)

Interagire avec les mains
![alt text](image-71.png)

Si vous fait un jeu VR
![alt text](image-72.png)

C est nouveau pour moi mais vous pouvez ajouter les cameras
![alt text](image-73.png)

On veut voir les mains plus en details
![alt text](image-74.png)


Il y a plein de Blocks qui chaqun necessite 1-5 jours de cours.
On ne les vera donc pas ;)

Mais si vous voulez vous rendre emplyable les connaitres est uen bonne idea.


Bon dans la theory, on pourrait faire play pour jouer a notre jeu.

Mais on a pas installer les applications pour faire de la VR et pas configurer notre casque en Oculus Link.


Pas de message  derreur mais un ecran noir qui bouge pas.

Essayons de builder pour le Quest un APK puis on regardera comment le jouer sur le PC directement.

Je vous invite a ajouter un cube et un sol dans votre scene
Pour voir si votre apk a fonctionner.


![alt text](image-75.png)




----------------------------------

Pour aller plus loin, il faut configurer votre casque en mode developpeurs.
Ce qui est deja faire avec les casques de la formation.
Si c est pas le cas, il faut le faire. 

Checher un video sur Youtube qui vous explique comment faire.
- Creer un compte meta developer
- Ajouter la double authentification
- Ajouter une organisation
- Creer une app
- Aller sur votre telphone
- Pairer le casque a votre compte developpeur
- Aller dans le option
- Toggle developer mode.

En Gros.


Maintenant il faut que votre casque soit autoriser de discuter avec votre oridinateur.

Bancher les casques et essayer d avoir ce menu

![alt text](image-76.png)
![alt text](image-77.png)

Toujours authoriser histoire de pas valider a chaque fois.

Android est un peu debile de ce coter la.
De fois, il faut redermer le casque et brancher debrancher jusqua ce que le message arrive.

Si il arrive pas cest que le casque est developer mais un setting interne a deconner. Faut le desactiver et reactiver comme developer.

Une fois valider 

Buildons notre APK.
![alt text](image-78.png)


Tant que vous avez pas valider le message.
Vous aurez ceci
![alt text](image-79.png)


------------

Bon ja vais preter mon casque a une personn.e
Je dois donc le Factory Reset
https://www.meta.com/en-gb/help/quest/149134797159340/
Power et volume -

De fait repartir pour un cafee a updated a la dernier version


Pendant que cela ce build
on peut aller verifier que c est app sont installer
- Godot Engine
- Open Source
- Open Blocks
- Steam Link
- ALVR
- Virtual desktop💲
- HDMI LINK
- First encounter
- Hello Qyest et Hand**

----------


20 Minutes plus tard
![alt text](image-80.png)

Faut savoir que ILCCP permet de builder moins vite...
Apres la premier fois.

ET a chaque fois que vous reseter certain paramettre de Unity
Cest pour cela que cest mieux d avoir un PC assez puissant qui fait tourner la VR...
Et qui soit pas un laptop.

Les laptops on un carte graphique brider pas suffisante pour la VR meme a 2200 Euro le laptop.
Autant avoir une petit tour a 1200 bien configurer.


----------

![alt text](image-81.png)


If you see that it means that we are good
![alt text](image-82.png)



Choisisez zone stationaire ou configurer le guardian room pour pouvoir bouger dans la piece. ;)




Vous voila heureux proprietaire d un application de realite augmenter en Oculus Quest sous Unity.

Fecilisations.

-


Changer la couleur du cube et rebuilder pour voir.
![alt text](image-83.png)


Normalement du fait d avoir utiliser IL2CPP  
cela ne devrait plus faire 27 minutes mais 1-2 minutes.   


Toke me 4
![alt text](image-84.png)



Manifiique mais c est lourd.
Si comme moi vous n avez pas un PC pour faire tourner la VR.
Alors vous devez travailer par boite a outils.

Creer des outils pour la VR dans des projets Non vr.
Puis les tester une fois que ca vous semble fonctionnel.

Bon ici dans la formation vous avec un PC puissance.
Donc allons voir comment on fait pour jouer a la VR sur votre PC.


-----------------


# Oculus Setup

