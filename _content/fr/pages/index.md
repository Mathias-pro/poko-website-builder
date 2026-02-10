---
translationKey: index
lang: fr
createdAt: 2026-02-09T13:18:00.000Z
uuid: b295be3b6780
localizationKey: 364680cddfc8
name: Tuto POKO
eleventyNavigation: null
metadata: null
preview: null
tags: []
status: ''
pageLayout: ''
generatePage: ''
vars: null
dataList: []
---
# Comment utilise-t-on POKO ?

Avant toute chose, crée toi un compte [Github](https://github.com/) et 1 compte [Cloudflare](https://www.cloudflare.com). « C’est entièrement gratuit »

## 1ère étape :

Aller sur cette page Github : [poko-website-builder](https://github.com/m4rrc0/poko-website-builder)

Vérifie bien que tu es connecté sur ton compte.

Première chose à faire cliquer sur**&#32;"Fork"**.

{% image src="/_images/fork.webp" %}

Tu peux ajouter une description à ton nouveau projet et le renommer.

Puis clique sur "**_&#160;Create fork "_** pour valider.

Tu obtiens un nouvel onglet avec une copie du **"** **website-builder "** qui sera sur ton nouveau compte Github .

{% image src="/_images/2-new-fork.webp", width="600" %}

" Félicitation c’est ton nouveau bébé ", prend en soins.

## 2éme étape :

Il te faut maintenant un **TOKEN.**[{% icon "undefined:undefined" %}](#_ftn1)

> **_Un TOKEN (ou jeton d’accès)_**_&#32;est une chaîne secrète utilisée à la place d’un mot de passe pour s’authentifier auprès de GitHub via l’API ou la ligne de commande; il donne des droits d’accès limités selon les permissions qu’on lui donne._

Tu pourras le créer en passant par ce lien [TOKEN](https://github.com/settings/personal-access-tokens/new?name=poko-website-builder+token&description=Read+and+write+repo+access+for+the+CMS&expires_in=none&contents=write).

#### Tu peux :

**1** Renommer ton TOKEN

**2** Mettre une description

**3** Définir le propriétaire

**4** Choisir une date d’expiration (si tu souhaites donner un accès temporaire)

{% image src="/_images/3-creation-de-token.webp", width="600" %}

**5** Choisir le type d’accès

**6** Choisir le type d’accès

{% image src="/_images/4-creation-de-token-2.webp", width="600" %}

**7** Et enfin générer le TOKEN 

{% image src="/_images/5-creation-de-token-3.webp", width="200" %}

À savoir :

•	Si tu as bifurqué le dépôt dans une organisation, change le " Resource Ownerpour " correspondre au nom de ton organisation.

•	N’hésite pas à définir une date d’expiration ou à restreindre le " Repository access ".

Le but étant d’avoir un TOKEN de secours pour pouvoir accéder à ton projet de n’importe où (garde bien une date d’expiration illimitée). 

Bravo, tu as créé ton premier TOKEN. 

{% image src="/_images/6-token.webp", width="600" %}

Copiez la valeur du TOKEN "**&#32;1** " et enregistrez-la dans un endroit sûr. (comme un gestionnaire de mots de passe).

•	⚠️ Ne partagez pas ce jeton avec qui que ce soit.

•	⚠️ Vous ne serez pas en mesure de lire le jeton de Github après avoir quitté la page (vous pouvez toujours en créer un nouveau cependant).

## 3éme étape :

On va maintenant héberger ton site web grâce à Cloudflare.

A) Clique sur ce lien pour commencer : [Workers & Pages.](https://dash.cloudflare.com/234702a4576e337d12ae62cabd002e0c/workers-and-pages)

B) Connecte-toi à ton compte  **1** , si ce n’est pas déjà fait.

C) Clique sur "_&#160;Ajouter "_**&#32;3**.

{% image src="/_images/7-workes-pages.webp", width="600" %}

> Sur cette page, tu pourras voir tous tes sites web hébergés sur Cloudflare via cet onglet " **2** ".

_D) Clique sur " Pages "_**&#32;4**.

E) Clique sur "_&#32;Importer un référentiel Git existant "_**&#32;5**.

{% image src="/_images/8-importer-un-referentiel-github.webp", width="400" %}

F) Clique dans le cadre _" Sélectionner un référentiel "_ **6** sur le nom de votre projet.

{% image src="/_images/9-chois-du-compte.webp", width="600" %}

G) Clique sur _" Commencer la configuration "_**&#32;7** (Il restera grisé temps que le projet ne sera pas sélectionné).

{% image src="/_images/10-commencer-la-configuration.webp", width="600" %}

H) Vérifie que tu es bien sur _" main "_ **8**.

{% image src="/_images/11-configurer-les-versions-et-les-deploiements.webp", width="600" %}

I)a) Dans _" Commande de version "_ écrit **" bun run build " 9**.

   b) Puis dans _" Répertoire de sortie de version_ écrit **" dist " 10**.

J) Clique sur _" Enregistrer et déployer "_**&#32;11**_._

{% image src="/_images/12-configurer-les-versions-et-les-deploiements-2.webp", width="600" %}

K) Patient un peu \~30s, tu devrais voir cette page s’afficher quand il a fini.

{% image src="/_images/13-operation-reussie.webp", width="400" %}

L) Clique sur _" Continuer le projet "_ **12**.

{% image src="/_images/14-modifier-ou-continuer.webp", width="600" %}

Si ça échoue, clique simplement sur _" Modifier les paramètres "_ **13**. L’erreur la plus commune étant de se tromper sur _" Commande de version " et " Répertoire de sortie de version_ écrit ".(voir étape I)

Si ça ne marche toujours pas clique sur l’onglet Workers & Pages à gauche, clique sur les _" … "_ **14** du site créé puis sur _"Paramètre"_ **15**.

{% image src="/_images/15.webp", width="600" %}

Supprime-le, puis refais la manipulation depuis le début, en validant bien chaque étape.

> Tu trouveras l'option de suppression tout en bas des paramètres **16**.

{% image src="/_images/16-suprimer.webp", width="600" %}

## 

## 4éme étape :

Ton site est maintenant hébergé ;p

On doit maintenant accéder au CMS  pour pouvoir le configurer.

- Trouvez l'URL de ton projet **1** _" Cloudflare Pages "_. (par ex. https://project-name.pages.dev)
- Ouvrez l'URL dans ton navigateur et ajoutez _" /admin "_ juste à la fin (Par ex. https://project-name.pages.dev/admin). Tu devrais voir l'écran de connexion CMS.

{% image src="/_images/17-cms-connection-admin.webp", width="500" %}

Clique sur _"Sign in with GitHub Using PAT"_ **2**.

{% image src="/_images/18-cms-connection-admin-2.webp", width="250" %}

Tu doit coller le TOKEN que tu as précieusement sauvegardé au début **3**.

{% image src="/_images/19-cms-connection-admin-token.webp", width="300" %}

Bienvenue sur ton CMS. 

> CMS : " Content managment systèm " est le système de gestion de ton site web.

On vas maintenant configurer celui-ci pour que tu puisse enfin commencer ton site.

Commence par aller dans _"settings"_ **4**.

{% image src="/_images/20-cms-pages-d-accueil-vide.webp" %}

A) Nomme ton site **5**.

B) Colle l’URL de ton site sans oublier le _" https:// "_ et en enlevant tout ce qui a après _" .dev "_ **6**.

{% image src="/_images/21-cms-settings-url.webp", width="300" %}

C) Ouvre le volet « Languages » et choisi ta langue.

{% image src="/_images/22-cms-settings-langue-1.webp", width="300" %}

{% image src="/_images/23-cms-settings-langue-2.webp", width="301" %}
