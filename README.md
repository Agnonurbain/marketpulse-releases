# MarketPulse — diffusion des versions Android

Ce dépôt contient uniquement les fichiers publics de diffusion de
l'application Android MarketPulse (relevé de prix fournisseurs) :

- l'APK de production de chaque version (`MarketPulse-<version>-<code>.apk`) ;
- `manifest.json`, le manifeste de mise à jour signé (Ed25519) lu par
  l'application ;
- les notes de version.

Il ne contient ni code source, ni clé, ni donnée.

## Mise à jour

À partir de la version 1.4.0, MarketPulse vérifie elle-même qu'une version
plus récente est publiée ici (`releases/latest/download/manifest.json`). Elle
ne propose une mise à jour qu'après avoir vérifié :

- la signature du manifeste ;
- l'identifiant de l'application et le certificat Android attendus ;
- la taille et l'empreinte SHA-256 de l'APK téléchargé.

L'installation est toujours confirmée par Android.

## Vérifier un APK téléchargé

- Identifiant : `com.opas.app.market_research`
- Empreinte SHA-256 du certificat de signature :
  `4a373b7b960e9acf86d04b399599c04050a5e401d3f71e6be73427e02d5002ef`
- Empreinte SHA-256 de l'APK : indiquée dans la publication et dans
  `manifest.json`.

N'installez jamais un fichier qui ne vient pas d'une publication de ce
dépôt, ou dont l'empreinte diffère.
