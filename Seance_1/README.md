# 3d_en_temps_reel

Une scène 3D interactive en temps réel construite avec **Three.js** et **WebGL**. 

## ✨ Fonctionnalités actuelles
* **Objets géométriques 3D :** Un ensemble de primitives (TorusKnot, Sphère, Torus, Cône) avec des matériaux métalliques et des couleurs vives.
* **Effets d'éclairage dynamiques :** Des lumières colorées (cyan et magenta) qui orbitent autour de la scène pour créer des reflets réalistes.
* **Environnement immersif :** Un système de particules flottantes servant de fond d'ambiance.
* **Interaction utilisateur soignée :** 
  * Un effet de "parallaxe" fluide : la scène entière s'incline en suivant les mouvements de la souris.
  * Un **curseur géométrique personnalisé** (losange animé) qui remplace la souris classique pour une expérience plus premium.

## 🚀 Comment lancer le projet ?
Pour visualiser la scène, il suffit de lancer un petit serveur web local dans ce dossier (par exemple avec l'extension *Live Server* de VS Code, ou avec la commande `npx serve` ou `python -m http.server`) et d'ouvrir le fichier `index.html`.