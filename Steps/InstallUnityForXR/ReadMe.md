

Téléchargeons le **Unity Hub** pour ne pas se casser la tête sur l’installation.  
![alt text](image-1.png)  
https://docs.unity.com/en-us/hub

Allons chercher la version de la formation :  
![alt text](image.png)  
https://unity.com/releases/editor/whats-new/6000.3.13f1

Allons dans **Install** et ajoutons avec le gestionnaire (à droite sur l’image) :  
- **Android Build Support**  
- **OpenJDK**  
- **Android SDK / NDK**  
![alt text](image-2.png)

Il nous faut aussi le **IL2CPP** pour Meta et pour pouvoir utiliser le Job System pour l’optimisation.  
![alt text](image-3.png)

Créons un projet.  
![alt text](image-4.png)

Il existe des templates de projet configurés pour la XR ou la VR.  
![alt text](image-5.png)

Nous, nous allons partir de zéro pour apprendre à configurer le projet sans outils inutiles.  
Utilisons un **URP Render Pipeline Blank Project**.  
![alt text](image-6.png)

Ces outils seront installés :  
![alt text](image-7.png)

On ne veut pas donner notre code à Unity.  
Créons un projet **Local**.  
![alt text](image-8.png)

Unity U/Q :  
![alt text](image-9.png)

Créons un projet sur GitHub que je vais appeler **HelloUnityA4**.  
![alt text](image-11.png)

Allons sauvegarder notre projet avec GitHub… vu que Unity ne me laisse pas faire.  
![alt text](image-14.png)  
![alt text](image-12.png)  
![alt text](image-13.png)  
![alt text](image-19.png)  
![alt text](image-15.png)

`2026_06_06_unity_hello_unity_a4`  
![alt text](image-17.png)

Bon, on peut aller créer un jeu en Godot pendant que Unity charge :  
![alt text](image-18.png)

Pendant que ça charge, on peut vérifier que le projet a bien été créé.  
![alt text](image-20.png)

Vous pouvez même prendre le temps de vous créer un repository à votre nom pour votre page d’accueil.  
[![alt text](image-21.png)](https://github.com/EloiStree)

Nous voilà dans Unity 3D.

Vérifions que nous avons un `.gitignore`.  
![alt text](image-22.png)

Petit `add` → `commit` → `pull` → `push`.

Vérifions que l’on voit les extensions de fichiers et les fichiers cachés.  
![alt text](image-23.png)

```bash
git status
```
(pour vérifier qu’il y a bien un `.gitignore` et pas de fichiers temporaires)

```bash
git add .
```

Un petit commit :  
```bash
git commit -m "Empty ready project"
```

Un petit `pull` / `push` pour le sauvegarder en ligne.

Si on fait de la merde…  
Vu que Unity n’a pas créé de README en ligne et a créé le projet local, il faut parfois forcer le push. Ce n’est pas forcément la meilleure manière.  
**Force Push**  
![alt text](image-25.png)

Essayons de retirer les packages qui ne servent à rien.  
![alt text](image-26.png)

Désactiver l’AI :  
![alt text](image-27.png)

Désactiver Cloth :  
![alt text](image-28.png)

Un par un, ça fait long. Allons directement dans le `manifest.json`.  
![alt text](image-29.png)

Évidemment, ça peut être dangereux de retirer des modules, mais ai-je besoin de ça dans mon projet ?

```json
"com.unity.modules.physics2d": "1.0.0",
"com.unity.modules.terrain": "1.0.0",
"com.unity.modules.terrainphysics": "1.0.0",
"com.unity.modules.wind": "1.0.0",
"com.unity.ai.navigation": "2.0.12",
```

![alt text](image-30.png)

Un petit **Add → Commit → Pull → Push** si vous n’avez rien cassé.  
![alt text](image-31.png)

Allons sur l’**Asset Store** de Unity.  
![alt text](image-32.png)

Et cherchons le **Meta XR SDK**  
(Ca change toujours de nom tous les ans, tapez « oculus meta xr »).  
![alt text](image-33.png)  
https://assetstore.unity.com/packages/sdk/meta-xr-sdk-9022845

Ajoutons les packages à notre projet ouvert.  
![alt text](image-34.png)

Quand vous suivez un tutoriel en ligne, regardez bien la version utilisée et les numéros d’OS du Quest (s’il est bien à jour).  
![alt text](image-35.png)

Cliquez sur **Installer** et allez boire un café 😉  
Ou faire un jeu sur Scratch :  
https://scratch.mit.edu/  
![alt text](image-36.png)  
![alt text](image-37.png)

Je vous laisse choisir si vous voulez partager avec Meta.  
![alt text](image-38.png)

Je vais skipper en fermant la fenêtre.  
![alt text](image-39.png)

On peut aller dans le menu, mais comme il nous le propose :  
![alt text](image-40.png)  
![alt text](image-41.png)

Avant de fixer les problèmes, il nous faut installer **OpenXR**.  
![alt text](image-42.png)  
![alt text](image-43.png)

Je suppose que oui du coup.  
![alt text](image-44.png)

Fixons ce que Unity XR Plugin nous propose.  
![alt text](image-45.png)  
![alt text](image-46.png)

Ça m’a téléchargé un XR Simulator.  
![alt text](image-47.png)

Mais je l’utilise peu à mon niveau. J’ai tendance à créer mes outils hors VR et à les tester en VR quand l’outil est prêt. Ce qui fait que je peux me passer du simulateur.

OK, validateurs bons. Allons faire un **Add → Commit → Pull → Push**.  
![alt text](image-48.png)

Allons configurer les paramètres du projet.  
![alt text](image-50.png)

Et validons ce qu’il nous reste à valider.  
![alt text](image-51.png)

Parlons de cela : on est encore sur Windows et pas sur Android.  
![alt text](image-53.png)  
![alt text](image-54.png)

Bon… Du coup, allons mettre notre projet en **Android** via **Build Profiles**.  
![alt text](image-55.png)  
![alt text](image-56.png)

**Coffee time**  
![alt text](image-57.png)

Changer pour Android peut modifier certains paramètres. Refaites un tour dans le menu précédent.  
![alt text](image-58.png)

Prenons la dernière version de C#.  
![alt text](image-59.png)

Si vous utilisez des serveurs externes (locaux ou des IA dans votre jeu, ex. : LLM Studio ou Flask Python) :  
![alt text](image-60.png)

Si votre application doit aller dans les fichiers du Quest pour chercher des images, vidéos ou avoir un dossier à la racine de la carte SD pour être plus facilement trouvable par l’utilisateur :  
![alt text](image-61.png)

**Be sure to use a unique package name for your APK**  
`pay.company.appuniquename`  
⚠️ **Alphanumérique uniquement** — pas d’espace ni de caractères spéciaux ⚠️  
![alt text](image-63.png)

---

Créons une scène vide.  
![alt text](image-49.png)

Puis ajoutons-la au prochain build.  
![alt text](image-64.png)

Retirons la caméra et allons dire bonjour au **Block de Meta**.  
![alt text](image-65.png)

**All the blocks**  
![alt text](image-66.png)

Ajoutons une caméra.  
![alt text](image-67.png)

Cela nous ajoute les composants tout chauds.

Ajoutons-y une sphère dans chaque main pour les voir (avec 1 ou 2 cm d’écart).  
![alt text](image-68.png)

On veut faire de la **réalité augmentée** avec le passthrough.  
![alt text](image-69.png)

On veut voir les manettes.  
![alt text](image-70.png)

Interagir avec les mains.  
![alt text](image-71.png)

Si vous faites un jeu VR :  
![alt text](image-72.png)

C’est nouveau pour moi, mais vous pouvez ajouter les caméras.  
![alt text](image-73.png)

On veut voir les mains plus en détail.  
![alt text](image-74.png)

Il y a plein de Blocks qui, chacun, nécessitent 1 à 5 jours de cours. On ne les verra donc pas 😉  
Mais si vous voulez vous rendre employable, les connaître est une bonne idée.

Bon, en théorie, on pourrait faire **Play** pour jouer à notre jeu.  
Mais on n’a pas installé les applications pour faire de la VR et on n’a pas configuré notre casque en Oculus Link.  
Pas de message d’erreur, mais un écran noir qui ne bouge pas.

Essayons de builder pour le Quest un APK, puis on regardera comment le jouer sur le PC directement.  
Je vous invite à ajouter un cube et un sol dans votre scène pour voir si votre APK fonctionne.  
![alt text](image-75.png)

---

Pour aller plus loin, il faut configurer votre casque en **mode développeur** (déjà fait avec les casques de la formation).  
Si ce n’est pas le cas, il faut le faire. Cherchez une vidéo sur YouTube qui vous explique comment faire :

- Créer un compte Meta Developer
- Ajouter la double authentification
- Ajouter une organisation
- Créer une app
- Aller sur votre téléphone
- Pairer le casque à votre compte développeur
- Aller dans les options → Activer le mode développeur

Maintenant, il faut que votre casque soit autorisé à discuter avec votre ordinateur.  
Branchez le casque et essayez d’avoir ce menu :  
![alt text](image-76.png)  
![alt text](image-77.png)

Toujours autoriser pour ne pas avoir à valider à chaque fois.  
Android est un peu pénible de ce côté-là. Parfois, il faut redémarrer le casque et rebrancher/débrancher jusqu’à ce que le message apparaisse.

**Buildons notre APK.**  
![alt text](image-78.png)

Tant que vous n’avez pas validé le message, vous aurez ceci :  
![alt text](image-79.png)

---

Bon, je vais prêter mon casque à une personne → **Factory Reset**  
https://www.meta.com/en-gb/help/quest/149134797159340/

Power + volume -  
De quoi repartir pour un café en attendant la dernière mise à jour.

Pendant que ça build, on peut aller vérifier que ces apps sont installées :
- Godot Engine
- Open Source
- Open Blocks
- Steam Link
- ALVR
- Virtual Desktop 💲
- HDMI LINK
- First Encounter
- Hello Quest et Hand Tracking

---

20 minutes plus tard…  
![alt text](image-80.png)

Faut savoir que **IL2CPP** permet de builder moins vite après la première fois, et à chaque fois que vous réinitialisez certains paramètres de Unity.  
C’est pour cela qu’il est mieux d’avoir un PC assez puissant qui fait tourner la VR… et qui ne soit pas un laptop.

![alt text](image-81.png)

If you see that it means that we are good.  
![alt text](image-82.png)

Choisissez **Zone stationnaire** ou configurez le **Guardian** pour pouvoir bouger dans la pièce. 😉

Vous voilà heureux propriétaire d’une application de réalité augmentée sur Oculus Quest faite avec Unity.  
**Félicitations !**

Changer la couleur du cube et rebuilder pour voir.  
![alt text](image-83.png)

Normalement, grâce à IL2CPP, ça ne devrait plus prendre 27 minutes mais 1 à 2 minutes.  
Moi : 4 minutes.  
![alt text](image-84.png)

Magnifique, mais c’est lourd.

Si comme moi vous n’avez pas un PC pour faire tourner la VR, vous devez travailler par boîtes à outils : créer des outils pour la VR dans des projets non-VR, puis les tester une fois qu’ils semblent fonctionnels.

---

# Oculus Setup

Allons chercher le logiciel de Meta pour installer **Oculus Link** sur votre ordinateur.  
[![alt text](image-85.png)](https://www.meta.com/be/en/quest/setup/)  
https://www.meta.com/be/en/quest/setup/

![alt text](image-86.png)

Note : c’est le bon moment pour mettre à jour les drivers de votre carte graphique.  
![alt text](image-87.png)  
![alt text](image-92.png)

Accepter de vendre votre âme…  
![alt text](image-88.png)

Choisir le dossier d’installation :  
![alt text](image-89.png)

Attendre…  
![alt text](image-90.png)  
![alt text](image-91.png)

Si vous voulez, vous pouvez commencer à installer **SteamVR** et **ALVR** pendant ce temps :  
https://github.com/alvr-org/ALVR  
https://store.steampowered.com/app/250820/SteamVR/

Ok, créer un compte si ce n’est pas déjà fait.  
![alt text](image-94.png)  
![alt text](image-93.png)

Setup nous propose de configurer notre casque par câble :  
![alt text](image-95.png)  
![alt text](image-96.png)  
![alt text](image-97.png)

Bon… On fera avec.  
![alt text](image-98.png)

Allons dans les paramètres développeur :  
![alt text](image-99.png)

Accepter toutes les options :  
![alt text](image-100.png)

Et acceptons les sources inconnues (applications non validées par un magasin).  
![alt text](image-101.png)

Si vous avez utilisé SteamVR, pour repasser en Quest Link, cliquez ici sur **OpenXR Runtime** :  
![alt text](image-102.png)

Ok, on est bon niveau setup.

Mais comme je dois vous montrer les interfaces du casque, il me faut un outil pour voir l’écran du casque…  
Il y a **scrcpy** :  
https://github.com/Genymobile/scrcpy/releases/tag/v4.0

![alt text](image-103.png)

Je le dézippe généralement dans un dossier que j’appelle `exe` à la racine.  
![alt text](image-104.png)

Ça vous permettra de faire des opérations sur votre casque et d’avoir la dernière version d’**ADB** (Android Debug Bridge).

---

**Lançons Oculus Link par câble**  
![alt text](image-114.png)

Si vous êtes dans une salle blanche, c’est que vous avez réussi à le faire tourner.  
![alt text](image-115.png)

Allons dans Unity et appuyons sur **Play**.  
![alt text](image-116.png)

**Ta dam !**  
Vous voilà avec une scène Unity via Quest Link 😉

---

**Prochaine étape** : Explorer les Inputs en VR, attraper un objet, puis apprendre à relocaliser une scène avec deux points.
