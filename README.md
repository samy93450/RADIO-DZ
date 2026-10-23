# LA VOIX D’ALGÉRIE — ASM TECHNOLOGIES

Application HTML et widget radio, adaptés notamment à l’iPhone 14 Plus. Passeport de face, cadre doré et inscriptions en relief.

## Publier sur GitHub Pages
1. Décompresser le ZIP sur votre ordinateur.
2. Créer un dépôt GitHub (exemple : `la-voix-algerie`).
3. Envoyer **le contenu du ZIP**, avec `index.html` directement à la racine du dépôt. Ne pas envoyer seulement le ZIP et ne pas ajouter de dossier parent.
4. Dans **Settings → Pages**, choisir **Deploy from a branch**, puis **main** et **/(root)**, et enregistrer.
5. Attendre la publication, puis ouvrir l’URL HTTPS indiquée par GitHub Pages.

Aucune compilation ni installation de dépendance. Tous les chemins d’icônes sont relatifs : fonctionnement à la racine ou sous le nom du dépôt. `.nojekyll` est fourni ; il peut être omis si votre interface d’envoi masque les fichiers commençant par un point, les fichiers du site n’en dépendent pas.

## Installer le raccourci sur iPhone 14 Plus
1. Ouvrir l’adresse **GitHub Pages publiée** dans Safari, et non la page du dépôt ou le fichier ZIP.
2. Toucher **Partager → Sur l’écran d’accueil** (ou **Ajouter à l’écran d’accueil**, selon iOS).
3. Vérifier l’icône carte d’Algérie et le nom « Voix d’Algérie », puis toucher **Ajouter**.
4. Si un ancien raccourci existe avec une autre icône, le supprimer et le recréer après actualisation du site. iOS peut conserver les anciennes icônes en cache.

L’icône personnalisée est déclarée explicitement avec `apple-touch-icon` en 180, 167 et 152 px. Le manifeste déclare aussi les icônes 192 et 512 px. Le rendu final et le cache appartiennent à iOS ; aucun site ne peut garantir une forme libre ou une transparence sur l’écran d’accueil. Le fichier PNG transparent original est fourni dans `icons/algerie-transparent.png`. Pour un rendu prévisible, la version Safari utilise cette même carte sur une tuile verte opaque ; iOS gère les coins arrondis.

## Fichiers
- `index.html` : application principale.
- `widget.html` : widget avec les mêmes fonctions radio.
- `apple-touch-icon.png` : icône Safari 180 px.
- `icons/` : carte transparente haute résolution, déclinaisons web et iOS.
- `favicon.ico` : icône navigateur et Windows.
- `manifest.webmanifest` : nom, lancement et icônes de l’application.

## Utilisation et limites
Cliquer le nom de station pour choisir une radio. Commandes : lecture/pause, arrêt, précédente/suivante, favoris. Le volume se règle avec les boutons physiques de l’iPhone ou les commandes du système.
Internet est nécessaire pour les radios et l’actualisation du catalogue. L’interface et la couverture sont incluses, sans CDN. Les 48 radios régionales sont référencées ; leurs adresses de flux sont recherchées à l’ouverture auprès de Radio Browser. Débits et disponibilité dépendent des diffuseurs. La reconnexion effectue jusqu’à six tentatives et change d’adresse de secours quand disponible. L’application ne transforme pas un flux 64 kb/s en véritable 320 kb/s.
Les favoris utilisent le stockage local du navigateur. Pas de garantie de lecture en arrière-plan ou écran verrouillé : cela dépend d’iOS. Pas de service worker afin d’éviter de figer les icônes ou flux en cache. La publication GitHub n’est pas réalisée par ce ZIP : elle nécessite les étapes ci-dessus.

## Références
- Icône Safari : https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html
- GitHub Pages : https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- Radios : https://radioalgerie.dz/player/fr et https://www.radio-browser.info/
