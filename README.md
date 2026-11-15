# SoraPrestige

Site de SoraPrestige : jets privés, yachts, clubs sportifs, personnalités, événements, hôtels et services à la carte.

En ligne sur **https://soraprestige.com** (hébergé par GitHub Pages, domaine chez IONOS).

Le site est statique : aucune dépendance, aucune compilation. Toute modification poussée sur la branche `main` est en ligne une à deux minutes plus tard.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | La page d'accueil (contenu, styles et scripts) |
| `404.html` | Page affichée pour une adresse inexistante |
| `favicon.svg` | Icône de l'onglet |
| `robots.txt`, `sitemap.xml` | Référencement dans les moteurs de recherche |
| `CNAME` | Domaine personnalisé pour GitHub Pages (ne pas supprimer) |

## Modules de la page

- **Formulaire de demande** (en haut de page) : six types de demande, champs obligatoires vérifiés, dates au format calendrier, devise du devis, précisions libres. Il prépare un message et l'ouvre dans WhatsApp ou dans la messagerie du visiteur ; rien n'est envoyé à un serveur. Le brouillon est gardé dans le navigateur du visiteur.
- **Estimateur de vol** (`#estimation`) : distance et durée de vol indicatives entre deux villes de la liste, pour un jet léger, intermédiaire et long-courrier, avec le type conseillé. Le bouton « Demander ce vol » pré-remplit le formulaire.
- Menu adapté au mobile, bouton WhatsApp flottant, retour en haut de page, lien actif dans le menu, bandeau de destinations, apparition progressive des sections (désactivée si le visiteur a demandé moins d'animations).

## Réglages

- **WhatsApp et e-mail du formulaire** : constantes `WHATSAPP` et `EMAIL` au début du script, en bas de `index.html`. Les mêmes coordonnées apparaissent dans la section contact, le pied de page, le bouton flottant et les données structurées (`application/ld+json`, dans `<head>`) : les changer partout.
- **Villes proposées** (formulaire et estimateur) : tableau `CITIES` dans le script, avec le nom affiché, la latitude et la longitude.
- **Vitesses et autonomies de l'estimateur** : tableau `JETS` dans le script.

## Photos

Les emplacements photo affichent pour l'instant un visuel décoratif. Pour mettre une vraie photo, déposer le fichier dans un dossier `images/` et ajouter la balise juste après `<figure class="media …">` dans la section concernée :

```html
<img src="images/jet.jpg" alt="Jet privé sur le tarmac">
```

## À compléter

Ces éléments sont **masqués** sur le site tant qu'ils ne sont pas renseignés (rien d'inventé n'est affiché) :

- **Équipe et chiffres clés** : section précédée du commentaire « SECTION MASQUÉE » ; remplir les crochets puis retirer l'attribut `hidden`.
- **Logos partenaires et témoignages** : même principe, section suivante.
- **Langues, horaires, bureaux** : lignes en commentaire dans la section Destinations.
- **Mentions légales, conditions générales** : liens en commentaire dans le pied de page (la page `confidentialite.html` est en ligne). Les mentions légales sont obligatoires pour un site professionnel en France : créer les pages puis décommenter les liens.

Les tarifs affichent « Sur devis » et la commission partenaires « Sur chaque voyage réalisé » ; ils peuvent être remplacés par des montants dans `index.html`.
