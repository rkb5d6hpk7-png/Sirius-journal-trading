# Sirius-journal-trading
Un jeu pour trader débutant 
SIRIUS TRADING JOURNAL — journal de trading Forex (application web locale)

CE QUE C'EST
Une application qui tient dans UN SEUL fichier : dist/index.html.
Pas de serveur, pas d'installation, pas de compte, aucune connexion Internet requise.
Vos données restent dans le navigateur de l'appareil. Elles ne sont PAS synchronisées
entre appareils et peuvent être perdues si les données du navigateur sont effacées :
exportez une sauvegarde (Paramètres > Sauvegarde complète) régulièrement.

UTILISER L'APPLICATION
- Ordinateur : double-cliquez sur dist/index.html (s'ouvre dans votre navigateur).
- iPhone : voir les explications données avec la livraison (lien hébergé).

CONTENU DU DOSSIER
  dist/index.html     l'application complète (fichier final)
  dist/artifact.html  même application, format de publication en page hébergée
  src/                code source (core.js = calculs, store.js = stockage, views-*.js = les 7 pages)
  test/core.test.js   73 tests des calculs, de la validation, de l'import/export et du CSV
  build.js            assemble src/ en dist/

COMMANDES (nécessitent Node.js 18 ou plus récent ; uniquement pour modifier le code)
  node build.js                      régénère dist/index.html
  node --test test/core.test.js      lance les tests des calculs

LIMITES CONNUES
- Calculs fondés sur des spécifications standard : 1 lot = 100 000 unités ; or (XAU/USD) = 100 onces.
  Votre courtier peut appliquer d'autres règles (taille de contrat, pas de volume, définition du pip).
- Paires croisées (sans la devise du compte) : le taux de conversion est saisi à la main.
- Les devises ne sont jamais converties ni additionnées : seule la devise active est comptée.
- Aucun ordre n'est passé, aucun courtier n'est connecté, aucun conseil financier n'est donné.
- Les statistiques décrivent le passé du journal et ne prévoient pas les résultats futurs.
- Pas de comptes ni de synchronisation cloud : cela demanderait un serveur (non inclus volontairement).
