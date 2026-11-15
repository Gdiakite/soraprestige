# SoraTrave Prestige

Page d'accueil de SoraTrave Prestige : jets privés, yachts, clubs sportifs, personnalités, événements, hôtels et services à la carte.

Le site est une seule page statique (`index.html`), sans dépendance ni étape de compilation. Le formulaire prépare un message et l'ouvre dans WhatsApp ou dans la messagerie du visiteur ; aucune donnée n'est stockée.

## Mettre en ligne avec GitHub Pages

1. Créer un dépôt sur GitHub (par exemple `soratrave-prestige`) et y déposer `index.html` et `README.md`.
2. Dans le dépôt : **Settings → Pages → Build and deployment → Source : Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
3. Après une à deux minutes, le site est accessible à l'adresse `https://<votre-compte>.github.io/soratrave-prestige/`.
4. Pour un nom de domaine propre (par exemple `prestige.soratrave.com`) : ajouter le domaine dans **Settings → Pages → Custom domain**, puis créer chez votre registrar un enregistrement DNS `CNAME` de `prestige` vers `<votre-compte>.github.io`.

## À compléter avant l'ouverture au public

Tout ce qui est entre crochets dans `index.html` est un emplacement à remplir :

- tarifs (`[VOTRE TARIF]`), commission partenaires (`[VOTRE COMMISSION]`) ;
- villes, pays, langues, horaires, bureaux, délai de réservation ;
- photos (`[PHOTO : …]`), logos partenaires, témoignages, noms des conseillers, chiffres clés ;
- liens vers les mentions légales, les conditions générales et la politique de confidentialité.

## Réglages

Le numéro WhatsApp et l'adresse e-mail du formulaire se changent en bas de `index.html`, dans les constantes `WHATSAPP` et `EMAIL`. Les mêmes coordonnées apparaissent aussi dans la section contact et le pied de page.
