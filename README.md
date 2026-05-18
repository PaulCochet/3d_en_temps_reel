# ✈️ SkyExperience - 3D en Temps Réel avec Three.js

Bienvenue dans ce dépôt dédié à la création d'expériences 3D interactives en temps réel. Ce projet retrace un parcours d'apprentissage structuré et progressif autour de **Three.js** et de **WebGL**, culminant par la réalisation d'une landing page de luxe haut de gamme : **SkyExperience**.

---

## 📁 Structure du Projet

Le dépôt est organisé en plusieurs dossiers représentant les étapes clés du développement :

*   **`Seance_1/` : Fondations de Three.js**
    *   Initiation aux scènes, caméras, moteurs de rendu WebGL et géométries de base.
    *   Création d'objets géométriques 3D primitifs (`TorusKnot`, `Sphere`, `Torus`, `Cone`) avec des matériaux métalliques brillants.
    *   Système d'éclairage dynamique avec lumières colorées (cyan et magenta) orbitant autour des objets.
    *   Ajout d'un système de particules flottantes d'ambiance en arrière-plan.
    *   Interaction utilisateur : Effet de parallaxe réactif à la souris et curseur géométrique personnalisé en losange animé.
*   **`Seance_2/` : Modèles & Intégration**
    *   Techniques de chargement de modèles 3D complexes.
    *   Expérimentations autour des animations liées au défilement (Scroll) et positionnement de la caméra.
    *   Développement de prototypes de "Hotspots" projetés en temps réel de coordonnées 3D mondiales en coordonnées 2D d'écran HTML.
*   **`Projet_final/` : SkyExperience - Luxury Aviation**
    *   Le chef d'œuvre final. Une landing page immersive et interactive dédiée à l'aviation privée d'exception.

---

## ✨ Projet Final : SkyExperience - Luxury Aviation

La landing page **SkyExperience** réunit l'ensemble des compétences acquises pour concevoir une interface de marque luxueuse et interactive.

### 🚀 Fonctionnalités Techniques Clés

#### 1. Chargement de Modèle & Texturing Personnalisé
*   **Modèle 3D Réaliste :** Chargement dynamique d'un modèle d'avion de ligne (`Avion.obj`) à l'aide de `OBJLoader`.
*   **Ajustement Géométrique Dynamique :** Recentrage complet et automatique de la géométrie de l'avion dès son chargement (via `Box3` et `translate`) pour garantir des rotations parfaites et sans décalage par rapport à ses axes.
*   **Matériaux Premium (PBR) :** Application de textures spécifiques (`Floquage.png` pour la carlingue et `Grosse_aile.png` pour les ailes) avec une configuration fine de la réflectivité (`metalness`), de la rugosité (`roughness`) et de l'intensité lumineuse d'environnement.

#### 2. Animation d'Entrée Immersive ("Intro Drop")
*   Au chargement initial de la page, l'avion effectue une descente majestueuse depuis le ciel (axe Y) vers sa position d'accueil, créant un effet d'atterrissage élégant dès les premières secondes.

#### 3. Système d'Animation Scroll-Linked à 4 États
Le comportement de l'avion et de la caméra s'adapte en temps réel à la progression du défilement de l'utilisateur grâce à des interpolations fluides (`lerp`) et un amortissement personnalisé (`easeInOutCubic`) :
*   **État 1 (Hero Section) :** L'avion se présente de face sous un angle majestueux, survolant l'arrière-plan textuel monumental "POLLUX".
*   **État 2 (Story Section) :** L'avion recule et s'incline en arrière-plan, laissant la place à un superbe **Bento Layout** (grille 2x2 vitrée) qui présente l'histoire et les valeurs de la compagnie avec des images haute qualité interactives.
*   **État 3 (Hotspots Section) :** L'avion pivote de profil (90°). Trois **hotspots interactifs** (Cockpit, Turboréacteur, Empennage) apparaissent au-dessus des parties clés de l'appareil. Leurs positions 2D sur l'écran sont calculées dynamiquement à chaque frame à partir de leurs coordonnées 3D dans le monde.
*   **État 4 (Final Focus Section) :** L'avion se recentre élégamment à une échelle ajustée pour inviter l'utilisateur à cliquer sur le Call-To-Action final ("Prendre un vol") animé par des pulsations lumineuses.

#### 4. Design & UI/UX Premium
*   **Direction Artistique :** Palette raffinée (bleus profonds, cyan éclatant, blancs épurés) et typographies soignées (`Playfair Display` pour l'élégance éditoriale, `Poppins` pour la clarté moderne).
*   **Effets Visuels :** Cartes Bento en verre dépoli (`backdrop-filter`), effets de survol interactifs avec zoom sur les images, et boutons à impulsions animées.
*   **Entièrement Responsive :** Adaptation fluide de la mise en page CSS et mise à jour dynamique du ratio de la caméra de rendu WebGL lors du redimensionnement de l'écran.

---

## 🛠️ Technologies Utilisées

*   **Three.js (v0.160.0)** - Rendu 3D WebGL
*   **JavaScript (ES Modules)** - Logique et interactivité
*   **HTML5 / CSS3** - Structure sémantique, disposition Flexbox/Grid et animations CSS
*   **Google Fonts** - Typographies premium (`Playfair Display`, `Poppins`)

---

## 🚀 Comment Lancer le Projet ?

Pour lancer et explorer le projet localement :

1.  **Cloner le dépôt :**
    ```bash
    git clone https://github.com/PaulCochet/3d_en_temps_reel.git
    cd 3d_en_temps_reel
    ```
2.  **Lancer un serveur web local :**
    Le chargement de textures et de modèles 3D (`.obj`) nécessite un serveur HTTP local pour éviter les restrictions de sécurité du protocole `file://` (erreurs CORS). Vous pouvez utiliser au choix :
    *   L'extension **Live Server** sur VS Code.
    *   La commande Python :
        ```bash
        python -m http.server 8000
        ```
    *   La commande Node.js / npx :
        ```bash
        npx serve
        ```
3.  **Ouvrir dans le navigateur :**
    Accédez à l'adresse indiquée (ex: `http://localhost:8000`) et naviguez vers le dossier `/Projet_final` pour vivre l'expérience **SkyExperience**.
