# Applications CHEFJEAN

Adresse unique à communiquer aux équipes : **https://chefjean.github.io/chefjean-carte/**

Cette racine est un portail : il liste les applications et ne change pas quand une
application s'ajoute. Chaque application est autonome (polices, logo et pictogrammes
embarqués), sans compte ni connexion.

| Application | Adresse | Rôle |
|---|---|---|
| Carte du jour | `/carte/` | Cocher les produits en stock, imprimer la carte A4 de la boutique. |
| Plats disponibles | `/plats/` | Fiche des plats seuls par famille (formats A et B). |
| Étiquettes du jour | `/etiquettes/` | Imprimer seulement les étiquettes nécessaires, format clinique 8 × 4 cm ou boutiques 17 × 3,5 cm. |

Régénération : chaque matin à 9h (heure de Paris), la tâche du matin reconstruit la carte,
les plats et les étiquettes, puis pousse ici. Un rafraîchissement de mi-journée republie
les trois applications et les données des étiquettes (`etiquettes/data.json`).

Le bouton **« Réactualiser »** de l'application Étiquettes recharge `etiquettes/data.json` :
il récupère la dernière version publiée, pas une lecture en direct du site.
