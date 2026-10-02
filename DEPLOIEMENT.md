# OxenFlace — Guide rapide

> Le site est maintenant composé de 3 éléments à garder ensemble dans le même dossier :
> `index.html`, le dossier `fonts/` (polices auto-hébergées, 100% hors-ligne) et le
> dossier `images/` (votre logo). Déployez toujours le dossier complet, pas seulement
> `index.html`.

## 1. Activer le formulaire de contact (5 min, gratuit, sans compte classique)

Le formulaire envoie les messages vers **oxenflace@gmail.com** via le service gratuit
**Web3Forms**, qui gère automatiquement le spam et les limites — aucune inscription
classique, juste une clé d'accès envoyée par email.

1. Allez sur **https://web3forms.com**
2. Entrez `oxenflace@gmail.com` dans le champ "Access Key" → cliquez sur "Create Access Key"
3. Une clé (ex: `a1b2c3d4-....`) est envoyée à cette adresse email — copiez-la
4. Ouvrez `index.html`, cherchez la ligne :
   ```
   formData.append('access_key', 'REMPLACER_PAR_VOTRE_CLE_WEB3FORMS');
   ```
   et remplacez `REMPLACER_PAR_VOTRE_CLE_WEB3FORMS` par votre clé.
5. Sauvegardez. C'est prêt — chaque message du site atterrit dans la boîte mail.

Le formulaire inclut déjà :
- un champ piège invisible (honeypot) qui bloque les robots basiques,
- la protection anti-spam intégrée de Web3Forms,
- une limite gratuite large, suffisante pour un site vitrine freelance.

## 2. Déployer le site gratuitement

Choisissez l'une de ces options (aucune ne nécessite de carte bancaire) :

### Option A — Netlify (le plus simple)
1. Allez sur https://app.netlify.com/drop
2. Glissez-déposez le dossier `oxenflace` (contenant `index.html`) dans la page
3. Le site est en ligne immédiatement, avec une adresse en `.netlify.app`
4. Vous pouvez ensuite relier un nom de domaine personnalisé si besoin

### Option B — GitHub Pages
1. Créez un dépôt GitHub, ajoutez-y `index.html`
2. Dans les paramètres du dépôt → "Pages" → activez le déploiement depuis la branche `main`
3. Le site est en ligne à l'adresse `https://votre-nom.github.io/nom-du-depot`

### Option C — Cloudflare Pages
1. Sur https://pages.cloudflare.com, créez un projet et importez le dossier
2. Déploiement automatique, gratuit, avec certificat HTTPS inclus

## 3. Polices et logo

- Les polices (**Poppins**, **Carlito**, **Liberation Mono**, **Lora Italic**) sont
  fournies en fichiers `.ttf` dans `fonts/` et chargées via `@font-face` avec des
  chemins relatifs : aucune requête vers Google Fonts ou un autre service, le site
  fonctionne même sans connexion internet une fois déployé.
- Le logo (`images/logo.png`) est votre image d'origine, recadrée et exportée en
  fond transparent pour bien ressortir sur le thème sombre. Il est utilisé dans le
  menu, le pied de page et comme favicon (`images/favicon.png`).

## 4. Personnaliser le contenu

- **Créations** : remplacez les 3 projets d'exemple par vos vraies réalisations
  (titre, description, technologies, et idéalement une capture d'écran à la place
  du numéro affiché dans la vignette).
- **Témoignages** : remplacez les 3 témoignages d'exemple par de vrais retours clients.
- Le reste (logo, couleurs, coordonnées) est déjà rempli avec vos informations.
