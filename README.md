# AMELHENS — Observatoire botanique (prototype 0.1)

## Inclus
- PWA installable Android (sans Play Store), sous réserve de publication HTTPS.
- Inventaire local via IndexedDB.
- Fiches végétaux : noms français/latins, famille, statut, secteur, provenance, date, GPS, photo et notes.
- Reconnaissance photo via API Pl@ntNet (connexion Internet et clé API personnelle nécessaires).
- Export CSV et sauvegarde/restauration JSON.
- Cache de l'interface pour utilisation hors connexion.

## Déploiement gratuit recommandé : GitHub Pages
1. Créer un compte GitHub gratuit.
2. Créer un dépôt public nommé `amelhens-observatoire`.
3. Décompresser l'archive et téléverser tous les fichiers et le dossier `icons` à la racine du dépôt.
4. Dans Settings > Pages, choisir le déploiement depuis la branche `main`, dossier `/ (root)`.
5. Attendre la publication. GitHub Pages fournit une adresse HTTPS.
6. Ouvrir cette adresse dans Chrome sur Android > menu ⋮ > « Installer l'application » ou « Ajouter à l'écran d'accueil ».

## Reconnaissance Pl@ntNet
1. Créer un compte développeur gratuit sur https://my.plantnet.org/
2. Créer une clé API.
3. Dans les paramètres de la clé, activer l'accès navigateur/CORS et autoriser exactement le domaine GitHub Pages de l'application.
4. Coller la clé dans Réglages de l'application.

Le plan gratuit Pl@ntNet annonce 500 identifications par jour. Les appels nécessitent Internet. La clé est stockée localement dans le navigateur de cet appareil. Ne pas publier une clé dans une application ouverte à d'autres utilisateurs sans architecture serveur adaptée.

## Mises à jour
Modifier les fichiers du dépôt GitHub : la version hébergée sera mise à jour. Le service worker utilise un cache versionné ; pour forcer une nouvelle version après modification, changer `amelhens-shell-v1` dans `sw.js` (ex. v2). Fermer puis rouvrir l'application après la mise à jour.

## Limites importantes du prototype
- Il s'agit d'une première version fonctionnelle, pas encore d'un outil scientifique validé ni d'un produit audité en sécurité.
- Les données sont stockées sur ce téléphone et dans ce navigateur : vider les données du navigateur ou désinstaller l'application peut les supprimer. Faire des sauvegardes JSON régulières.
- Pas encore de synchronisation multi-appareils, gestion des lots de semences, mesures dendrométriques, suivi hydrologique avancé, cartographie de parcelles ni analyse scientifique statistique.
- La détermination automatique doit toujours être vérifiée. Les scores ne sont pas des probabilités garanties.
- La géolocalisation et l'installation PWA nécessitent HTTPS et l'autorisation Android.

## Gratuité
Le code est fourni sans frais. GitHub Pages et le niveau gratuit de l'API Pl@ntNet sont utilisés dans les limites de leurs conditions et quotas, qui peuvent évoluer.
