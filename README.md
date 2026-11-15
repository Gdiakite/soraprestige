# SoraPrestige

Site de SoraPrestige : jets privés, yachts, clubs sportifs, personnalités, événements, hôtels et services à la carte.

En ligne sur **https://soraprestige.com** (hébergé par GitHub Pages, domaine chez IONOS).

Le site est statique : aucune dépendance, aucune compilation. Toute modification poussée sur la branche `main` est en ligne une à deux minutes plus tard.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | La page d'accueil (contenu, styles et scripts) |
| `confidentialite.html` | Politique de confidentialité |
| `404.html` | Page affichée pour une adresse inexistante |
| `images/` | Photos du site et image d'aperçu pour les réseaux sociaux (`og.jpg`) |
| `favicon.svg` | Icône de l'onglet |
| `robots.txt`, `sitemap.xml` | Référencement dans les moteurs de recherche |
| `CNAME` | Domaine personnalisé pour GitHub Pages (ne pas supprimer) |

## Modules de la page

- **Formulaire de demande** : sept types de demande (dont Visa), champs obligatoires vérifiés, dates au format calendrier, devise du devis, précisions libres. Il prépare un message et l'ouvre dans WhatsApp ou dans la messagerie du visiteur ; rien n'est envoyé à un serveur. Le brouillon est gardé dans le navigateur du visiteur.
- **Section Visas et formalités** (`#visas`) : prise en charge, aide-mémoire des documents, lien vers la demande Visa.
- **Estimateur de vol** (`#estimation`) : distance et durée de vol indicatives entre deux villes de la liste, pour un jet léger, intermédiaire et long-courrier, avec le type conseillé. Le bouton « Demander ce vol » pré-remplit le formulaire.
- Menu adapté au mobile, bouton WhatsApp flottant, retour en haut de page, lien actif dans le menu, apparition progressive des sections (désactivée si le visiteur a demandé moins d'animations).

## Direction artistique

Mise en page « magazine » : fond ivoire `#F3EEE4`, encre `#16130E`, accent bronze `#8B5E34`, sections sombres pour l'estimateur, les personnalités et le contact. Polices Google Fonts : **Bodoni Moda** (titres) et **Instrument Sans** (texte). Les couleurs sont des variables CSS au début du `<style>` de `index.html`.

Bodoni Moda dessine le trait d'union comme un filet presque invisible en grande taille : dans les titres en Bodoni, écrire `&#8208;` au lieu de `-` (ex. `Dites&#8208;nous`).

## Réglages

- **WhatsApp et e-mail du formulaire** : constantes `WHATSAPP` et `EMAIL` au début du script, en bas de `index.html`. Les mêmes coordonnées apparaissent dans la section contact, le pied de page, le bouton flottant et les données structurées (`application/ld+json`, dans `<head>`) : les changer partout.
- **Villes proposées** (formulaire et estimateur) : tableau `CITIES` dans le script, avec le nom affiché, la latitude et la longitude.
- **Vitesses et autonomies de l'estimateur** : tableau `JETS` dans le script.

## Photos

Les photos actuelles viennent d'Unsplash, sous [licence Unsplash](https://unsplash.com/license) (usage commercial gratuit, crédit non obligatoire) :

| Fichier | Sujet | Photographe |
|---|---|---|
| `jet.jpg` | Jet privé au coucher du soleil (Napa) | Chris Leipelt |
| `yacht.jpg` | Yacht au large de Cannes | redcharlie |
| `vip.jpg` | Berline Mercedes Classe S | Unsplash (page `pgWzo-bNUeM`) |
| `evenement.jpg` | Table de gala aux bougies | Unsplash (page `fb0_wj2MZk4`) |
| `hotel.jpg` | Suite avec bain, Banyan Tree Macau | Dynamic Hong Kong |
| `clubs.jpg` | Terrain de football de nuit (Suède) | Jonathan Petersson |

Pour utiliser vos propres photos, remplacez le fichier dans `images/` en gardant le même nom (format paysage, environ 1600 à 2000 px de large, moins de 400 Ko), et adaptez le texte `alt` dans `index.html`.

## À compléter

Ces éléments sont **masqués** sur le site tant qu'ils ne sont pas renseignés (rien d'inventé n'est affiché) :

- **Équipe et chiffres clés** : section précédée du commentaire « SECTION MASQUÉE » ; remplir les crochets puis retirer l'attribut `hidden`.
- **Logos partenaires et témoignages** : même principe, section suivante.
- **Langues, horaires, bureaux** : lignes en commentaire dans la section Destinations.
- **Mentions légales** : lien en commentaire tout en bas de page, à côté de « Confidentialité » (la page `confidentialite.html` est en ligne). Les mentions légales sont obligatoires pour un site professionnel en France : créer les pages puis décommenter les liens.

Les tarifs affichent « Sur devis » et la commission partenaires « Sur chaque voyage réalisé » ; ils peuvent être remplacés par des montants dans `index.html`.
