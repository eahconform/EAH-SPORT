
# EAH SPORT
### Personal Coaching Experience

![EAH SPORT](logo.png)

**Votre progression. Votre programme. Votre coach.**

EAH SPORT est une plateforme de coaching sportif connectée développée par EAH Conformité.

Elle permet aux coachs sportifs de proposer à leurs clients un espace personnel accessible directement depuis une carte NFC.

La plateforme est administrée depuis Google Sheets, sans avoir besoin de modifier le code du site internet pour actualiser les exercices et les programmes sportifs.

---

## 1. ACCÈS À LA PLATEFORME

### Site internet

https://eahconform.github.io/EAH-SPORT/

### Administration Google Sheets

https://docs.google.com/spreadsheets/d/1psuHRrKQaFlleYeG8CdhUot6szMS5G9-76bpDIbYlKo/edit

### Application Google Apps Script

https://script.google.com/macros/s/AKfycbzRqNkdk5gvHbIPtdRAGwxMfmMGX3yoCv4FnPUGPJA5qYVZAyUHUV8ODEiBIBD9AhQD/exec

---

## 2. FONCTIONNALITÉS

- 50 cartes NFC avec liens individuels.
- Activation de la carte au premier scan.
- Création d'un profil sportif personnel.
- Ajout d'une photo de profil.
- Accès automatique au profil depuis la carte.
- Message personnalisé du coach.
- Bibliothèque d'exercices sportifs.
- Photos interactives des exercices.
- Fiches techniques détaillées.
- Tutoriels vidéo.
- Recherche par nom d'exercice.
- Filtrage par groupe musculaire.
- Création de séances personnalisées.
- Attribution des séances aux sportifs concernés.
- Programmation des séries et répétitions.
- Personnalisation des charges par série.
- Gestion des temps de récupération.
- Activation et désactivation des cartes.
- Administration centralisée depuis Google Sheets.
- Interface adaptée aux smartphones, tablettes et ordinateurs.

---

## 3. COMMENT FONCTIONNE UNE CARTE NFC ?

Chaque carte NFC possède un lien unique contenant un token individuel.

Exemple :

https://eahconform.github.io/EAH-SPORT/?token=TOKEN_UNIQUE

Le token permet à la plateforme d'identifier la carte et de retrouver les informations associées dans Google Sheets.

### Premier scan

Lors du premier scan d'une carte disponible, le sportif accède à un formulaire d'activation.

Il renseigne :

- Nom
- Prénom
- Âge
- Poids en kilogrammes
- Taille en centimètres
- Nom du coach
- Adresse email
- Photo de profil facultative

Après validation, les informations sont transmises à Google Apps Script pour être enregistrées.

La carte devient active si le serveur confirme son activation.

### Scans suivants

Lorsque le sportif scanne de nouveau sa carte, son espace personnel s'ouvre automatiquement.

Il retrouve :

- Sa photo de profil.
- Ses informations personnelles.
- Le message de son coach.
- Ses séances personnalisées.
- La bibliothèque des exercices.
- Les tutoriels vidéo.

---

## 4. ADMINISTRATION GOOGLE SHEETS

Le Google Sheets est organisé en cinq onglets principaux.

| Onglet | Fonction |
|---|---|
| TABLEAU DE BORD | Statistiques générales |
| UTILISATEURS | Gestion des cartes et profils |
| EXERCICES | Bibliothèque des exercices |
| SEANCES | Création des programmes sportifs |
| PARAMETRES | Configuration de la plateforme |

Le coach doit disposer des droits de modification sur le Google Sheets.

---

## 5. TABLEAU DE BORD

Le tableau de bord permet de visualiser les principaux indicateurs de la plateforme.

- Nombre de cartes actives.
- Nombre de cartes disponibles.
- Nombre de cartes désactivées.
- Nombre d'exercices actifs.
- Nombre de lignes de séances.
- Taux d'activation des cartes.

Les statistiques sont calculées à partir des données des autres onglets.

En cas d'erreur #ERROR!, vérifier les formules Google Sheets et les paramètres régionaux du document.

---

## 6. GESTION DES UTILISATEURS

L'onglet UTILISATEURS permet de gérer les 50 cartes NFC et les profils sportifs.

Les informations associées aux utilisateurs comprennent notamment :

| Information | Description |
|---|---|
| ID | Identifiant unique du sportif |
| TOKEN | Clé individuelle de la carte |
| LIEN | Adresse à programmer sur la carte NFC |
| STATUT | État de la carte |
| NOM | Nom du sportif |
| PRENOM | Prénom du sportif |
| AGE | Âge du sportif |
| POIDS | Poids en kg |
| TAILLE | Taille en cm |
| COACH | Coach associé |
| EMAIL | Adresse email |
| PHOTO | Photo de profil |
| MESSAGE | Message personnalisé |

### Codes couleurs

| Couleur | Statut | Fonction |
|---|---|---|
| 🟢 Vert | ACTIF | Profil accessible |
| 🟠 Orange | DISPONIBLE | Carte à activer |
| 🔴 Rouge | DESACTIVE | Accès bloqué |

### Désactiver une carte

Pour désactiver une carte, modifier son statut dans Google Sheets.

Le serveur doit vérifier ce statut à chaque demande d'accès.

Ne pas supprimer ou modifier le token d'une carte déjà distribuée sans procédure de remplacement.

---

## 7. MESSAGE PERSONNALISÉ DU COACH

Le coach peut ajouter un message individuel dans la colonne MESSAGE de l'utilisateur.

Exemple :

> Bravo pour ta progression !
> Cette semaine, nous allons travailler davantage
> sur la force et la stabilité.
> Ta nouvelle séance est disponible.

Ce message apparaît directement dans l'espace personnel du sportif lors de la prochaine actualisation.

Chaque utilisateur peut recevoir un message différent.

---

## 8. CRÉATION DES EXERCICES

L'onglet EXERCICES constitue la bibliothèque sportive de référence.

Le coach peut ajouter, modifier ou désactiver des exercices.

Pour chaque exercice, renseigner les champs correspondants :

| Information | Exemple |
|---|---|
| Nom | Squat |
| Groupes musculaires | Quadriceps, Fessiers |
| Description | Fléchir les jambes en contrôlant la descente |
| Photo | images/squat.webp |
| Vidéo | Lien YouTube du tutoriel |
| Active | TRUE |

Les intitulés exacts des colonnes doivent rester compatibles avec le code Apps Script existant.

### Exemple de bibliothèque

| Exercice | Groupes musculaires |
|---|---|
| Squat | Quadriceps, Fessiers |
| Développé couché | Pectoraux, Triceps |
| Tirage vertical | Dos, Biceps |
| Soulevé de terre | Dos, Fessiers, Ischio-jambiers |
| Gainage | Abdominaux |
| Fentes | Quadriceps, Fessiers |
| Curl biceps | Biceps |
| Extension triceps | Triceps |
| Développé militaire | Épaules, Triceps |
| Presse à cuisses | Quadriceps, Fessiers |
| Hip thrust | Fessiers, Ischio-jambiers |
| Rowing | Dos, Biceps |

Il est possible d'enrichir progressivement la bibliothèque en ajoutant de nouvelles lignes.

---

## 9. PHOTOS INTERACTIVES

Chaque photo d'exercice est un bouton interactif dans la bibliothèque sportive.

Lorsque le sportif clique sur la photo, une fiche technique s'ouvre avec :

- Le nom de l'exercice.
- La photo de l'exercice.
- Les groupes musculaires sollicités.
- La description technique.
- Les consignes renseignées par le coach.
- Le tutoriel vidéo associé.
- Un bouton d'ouverture de la vidéo.

Le sportif peut également ouvrir cette fiche en cliquant sur le bouton Voir les détails.

Les informations proviennent de Google Sheets.

---

## 10. AJOUTER UNE PHOTO D'EXERCICE

### Méthode 1 : GitHub

Ajouter la photo dans le dossier images du dépôt.

Exemple :

images/squat.webp

Renseigner ensuite ce chemin dans la colonne photo de Google Sheets.

### Méthode 2 : Google Drive

1. Importer la photo dans Google Drive.
2. Configurer les autorisations de consultation.
3. Copier le lien de partage.
4. Coller le lien dans la colonne photo.

Les liens Drive sont convertis en liens de miniature par le site.

L'affichage dépend des autorisations et de la disponibilité du fichier.

### Méthode 3 : Image hébergée en ligne

Renseigner directement une URL HTTPS permettant d'accéder à l'image.

### Format recommandé

- Format : WEBP
- Dimensions : 1200 x 900 pixels
- Ratio : 4:3
- Poids conseillé : 80 à 200 Ko
- Qualité : haute définition

Utiliser uniquement des photos dont les droits d'utilisation sont autorisés.

---

## 11. AJOUTER UNE VIDÉO

Le coach peut ajouter un tutoriel vidéo en collant son lien dans la colonne vidéo de l'exercice.

### Plateformes compatibles

| Plateforme | Fonctionnement |
|---|---|
| YouTube | Lecteur intégré |
| YouTube Shorts | Lecteur intégré |
| Google Drive | Lecteur intégré |
| Vimeo | Lecteur intégré |
| MP4 | Lecteur intégré |
| WEBM | Lecteur intégré |
| Instagram | Ouverture externe |
| TikTok | Ouverture externe |
| Facebook | Ouverture externe |
| Autres liens HTTPS | Ouverture externe |

### Exemple YouTube

https://www.youtube.com/watch?v=IDENTIFIANT

### Exemple Google Drive

https://drive.google.com/file/d/IDENTIFIANT/view

### Exemple Instagram

https://www.instagram.com/reel/IDENTIFIANT/

Les vidéos doivent être accessibles aux sportifs concernés.

Certaines plateformes ou certains auteurs peuvent empêcher la lecture intégrée.

Dans ce cas, utiliser le bouton d'ouverture externe.

---

## 12. CRÉATION D'UNE SÉANCE SPORTIVE

L'onglet SEANCES permet au coach de créer des programmes personnalisés.

Chaque ligne correspond à un exercice d'une séance.

Pour créer une séance :

1. Renseigner le nom de la séance.
2. Sélectionner le ou les destinataires.
3. Choisir un exercice dans le menu déroulant.
4. Vérifier les groupes musculaires.
5. Vérifier le lien vidéo associé.
6. Renseigner le nombre de séries.
7. Renseigner les répétitions.
8. Renseigner les charges.
9. Renseigner les temps de récupération.
10. Ajouter les consignes éventuelles.
11. Activer la séance si une colonne ACTIVE existe.

Les groupes musculaires et la vidéo doivent être récupérés depuis la bibliothèque EXERCICES par les formules ou le script prévu à cet effet.

---

## 13. EXEMPLE DE SÉANCE

### Séance : Jambes - Force et volume

| Exercice | Séries | Répétitions | Charges | Repos |
|---|---:|---|---|---|
| Squat | 4 | 12/10/8/6 | 40/50/60/70 | 90 |
| Presse à cuisses | 4 | 12/12/10/10 | 80/90/100/110 | 90 |
| Hip thrust | 3 | 12/10/8 | 50/60/70 | 90 |
| Fentes | 3 | 12 | 15 | 60 |
| Gainage | 3 | 45 s | PDC | 30 |

Pour regrouper plusieurs exercices dans une même séance, utiliser exactement le même nom de séance sur les lignes correspondantes.

Les valeurs ci-dessus sont des exemples de fonctionnement et non des prescriptions universelles.

Le coach doit adapter les charges et les volumes au niveau de chaque sportif.

---

## 14. PERSONNALISATION DES SÉRIES

EAH SPORT permet de définir des répétitions et des charges différentes pour chaque série.

Utiliser le séparateur / entre les valeurs.

### Exemple

Nombre de séries :

4

Répétitions :

12/10/8/6

Charges :

40/50/60/70

Récupération :

60/90/90/120

### Résultat sur le profil

| Série | Répétitions | Charge | Récupération |
|---|---:|---:|---:|
| 1 | 12 | 40 kg | 60 s |
| 2 | 10 | 50 kg | 90 s |
| 3 | 8 | 60 kg | 90 s |
| 4 | 6 | 70 kg | 120 s |

Si une seule valeur est renseignée, elle sera appliquée à toutes les séries.

Exemple :

- Séries : 4
- Répétitions : 12
- Charges : 50
- Récupération : 90

Le sportif verra quatre séries de 12 répétitions à 50 kg avec 90 secondes de récupération.

Conseil : utiliser le format Texte brut dans les cellules contenant plusieurs valeurs séparées par / afin d'éviter leur conversion automatique en dates.

---

## 15. ATTRIBUTION DES SÉANCES

Le coach peut attribuer une séance à un sportif ou à plusieurs sportifs selon le format de destinataires pris en charge par Apps Script.

Utiliser les identifiants des sportifs présents dans l'onglet UTILISATEURS.

Exemple d'identifiant :

EAH-001

Pour une attribution multiple, respecter le séparateur défini dans le code Apps Script.

Toutes les lignes d'une séance doivent être attribuées aux destinataires concernés.

Le serveur Apps Script doit filtrer les séances avant de les transmettre au site.

Un sportif ne doit jamais recevoir les programmes privés des autres utilisateurs.

---

## 16. ACTUALISATION DES INFORMATIONS

Le site récupère ses données depuis Google Apps Script.

Lorsque le coach modifie Google Sheets, il n'est pas nécessaire de modifier le fichier index.html.

Les changements apparaissent :

- Lors de la prochaine ouverture du profil.
- Lors d'un nouveau scan NFC.
- Lorsque le sportif clique sur Actualiser.

Les modifications concernent notamment :

- Les exercices.
- Les photos.
- Les vidéos.
- Les descriptions.
- Les groupes musculaires.
- Les séances.
- Les charges.
- Les répétitions.
- Les messages du coach.
- Le statut des cartes.

---

## 17. ORGANISATION DU DÉPÔT GITHUB

EAH-SPORT/
│
├── index.html
├── README.md
├── logo.png
│
└── images/
    ├── squat.webp
    ├── developpe-couche.webp
    ├── tirage-vertical.webp
    ├── souleve-de-terre.webp
    ├── gainage.webp
    ├── fentes.webp
    ├── curl-biceps.webp
    ├── extension-triceps.webp
    ├── developpe-militaire.webp
    ├── presse-cuisses.webp
    ├── hip-thrust.webp
    └── rowing.webp

### Description des fichiers

index.html :
Interface principale de la plateforme.

README.md :
Documentation et guide d'utilisation.

logo.png :
Logo EAH Conformité.

images/ :
Bibliothèque des photos d'exercices.

---

## 18. ARCHITECTURE TECHNIQUE

EAH SPORT utilise quatre technologies principales.

### GitHub Pages

Hébergement du site internet.

### Google Apps Script

Communication entre le site et Google Sheets.

Gestion des demandes d'accès et d'activation.

### Google Sheets

Base de données et interface d'administration du coach.

### Google Drive

Stockage des médias lorsque cette méthode est configurée dans Apps Script.

### Schéma de fonctionnement

Carte NFC
    |
    v
Site EAH SPORT - GitHub Pages
    |
    v
Google Apps Script
    |
    +---- Google Sheets
    |
    +---- Google Drive

Le site utilise les actions API suivantes :

- read : récupération des informations associées au token.
- activate : activation d'une carte disponible.

Ces actions doivent correspondre aux fonctions réellement prises en charge par le serveur Apps Script.

---

## 19. CONFIGURATION GITHUB PAGES

1. Créer le dépôt EAH-SPORT.
2. Ajouter le fichier index.html.
3. Ajouter le fichier README.md.
4. Ajouter le logo.png.
5. Créer le dossier images.
6. Ouvrir Settings.
7. Sélectionner Pages.
8. Choisir Deploy from a branch.
9. Sélectionner main.
10. Sélectionner /root.
11. Cliquer sur Save.

Adresse prévue :

https://eahconform.github.io/EAH-SPORT/

Renseigner cette adresse dans les paramètres Google Sheets et vérifier les liens NFC avant leur programmation.

---

## 20. CONFIGURATION GOOGLE APPS SCRIPT

Pour publier une nouvelle version du serveur :

1. Ouvrir Google Apps Script.
2. Cliquer sur Déployer.
3. Sélectionner Gérer les déploiements.
4. Modifier le déploiement existant.
5. Sélectionner Nouvelle version.
6. Vérifier les autorisations.
7. Déployer.

Configuration prévue pour cette architecture :

- Type : Application Web.
- Exécuter en tant que : propriétaire.
- Accès : tout le monde, si autorisé par le compte.

L'accès public à l'application Web ne doit pas donner un accès public aux données privées.

Toutes les demandes doivent être contrôlées côté serveur.

En conservant le même déploiement, il est généralement possible de conserver la même URL /exec.

---

## 21. PROGRAMMATION DES CARTES NFC

Pour programmer une carte NFC :

1. Ouvrir l'onglet UTILISATEURS.
2. Identifier une carte disponible.
3. Copier son lien individuel.
4. Ouvrir une application d'écriture NFC.
5. Sélectionner l'enregistrement URL.
6. Coller le lien individuel.
7. Écrire le lien sur la carte.
8. Tester la carte avec un smartphone compatible.

Chaque carte doit posséder son propre lien.

Ne pas programmer le même token sur plusieurs cartes destinées à des utilisateurs différents.

Ne pas verrouiller définitivement une carte avant d'avoir vérifié son fonctionnement.

---

## 22. RÉSOLUTION DES PROBLÈMES

### Le site ne charge pas

Vérifier :

- L'adresse Apps Script.
- Le déploiement de l'application Web.
- Les autorisations.
- La connexion internet.
- La compatibilité des actions read et activate.

### Le tableau de bord affiche #ERROR!

Vérifier :

- Les paramètres régionaux du Google Sheets.
- Les séparateurs des formules.
- Les noms des onglets.
- Les références des colonnes.
- Les formules générées par Apps Script.

### Les groupes musculaires ou les vidéos affichent #ERROR!

Vérifier les formules de recherche dans l'onglet SEANCES.

Vérifier également que le nom de l'exercice correspond exactement à celui de la bibliothèque EXERCICES.

### Une photo ne s'affiche pas

Vérifier :

- Le nom du fichier.
- Son extension.
- Son emplacement dans GitHub.
- Les majuscules et minuscules.
- Les autorisations Google Drive.
- La validité du lien.

### Une vidéo ne s'affiche pas

Vérifier :

- Le lien vidéo.
- Les autorisations de consultation.
- La compatibilité de la plateforme.
- L'autorisation de lecture intégrée.

### Une séance ne s'affiche pas

Vérifier :

- L'identifiant du destinataire.
- Le nom de la séance.
- Le nom de l'exercice.
- Le statut de la séance.
- Le filtrage réalisé par Apps Script.

Cliquer ensuite sur Actualiser depuis le profil.

### La carte ne fonctionne pas

Vérifier :

- Le lien NFC.
- Le token.
- Le statut de la carte.
- L'adresse GitHub Pages.
- La compatibilité NFC du smartphone.

---

## 23. SÉCURITÉ ET CONFIDENTIALITÉ

Les données personnelles des sportifs doivent être protégées.

Recommandations :

- Ne jamais publier le Google Sheets en accès public.
- Limiter les droits de modification aux personnes autorisées.
- Ne jamais publier les tokens individuels sur GitHub.
- Utiliser des tokens uniques et difficiles à deviner.
- Vérifier les statuts et les autorisations côté serveur.
- Filtrer les séances côté serveur.
- Désactiver immédiatement une carte perdue.
- Protéger les photos personnelles.
- Effectuer des sauvegardes régulières.
- Informer les sportifs du traitement de leurs données.
- Prévoir une procédure de modification et de suppression des données.

Le lien NFC fonctionne actuellement comme une clé d'accès.

Toute personne disposant de ce lien peut potentiellement accéder au profil associé.

Une authentification supplémentaire par code PIN ou compte personnel est recommandée avant une exploitation commerciale.

La conformité au RGPD nécessite des mesures techniques et organisationnelles adaptées.

---

## 24. VÉRIFICATIONS AVANT MISE EN SERVICE

- [ ] GitHub Pages opérationnel.
- [ ] Application Apps Script déployée.
- [ ] Connexion entre le site et Apps Script vérifiée.
- [ ] Les 50 tokens sont uniques.
- [ ] Les 50 liens NFC sont corrects.
- [ ] Activation d'une carte test réussie.
- [ ] Photo de profil enregistrée.
- [ ] Message du coach affiché.
- [ ] Exercices correctement affichés.
- [ ] Photos interactives fonctionnelles.
- [ ] Tutoriels vidéo accessibles.
- [ ] Séances personnalisées affichées.
- [ ] Isolation des séances entre utilisateurs vérifiée.
- [ ] Désactivation d'une carte test réussie.
- [ ] Tableau de bord sans erreur.
- [ ] Colonnes GROUPES et VIDEO sans erreur.
- [ ] Confidentialité des données vérifiée.

---

## 25. ÉVOLUTIONS ENVISAGÉES

Les fonctionnalités suivantes pourront être ajoutées dans de futures versions :

- Historique des entraînements.
- Validation des séries réalisées.
- Suivi des performances.
- Graphiques de progression.
- Chronomètre de récupération.
- Modification du profil par le sportif.
- Messagerie coach et sportif.
- Notifications de nouvelles séances.
- Calendrier des entraînements.
- Authentification par code PIN.
- Gestion de plusieurs coachs.
- Abonnements sportifs.
- Export PDF des programmes.
- Statistiques individuelles.
- Suivi des objectifs sportifs.

Ces fonctionnalités ne sont pas incluses dans la version actuelle.

---

## 26. CONTACT ET ASSISTANCE

EAH CONFORMITÉ

Solutions digitales et cartes connectées NFC.

Email : goin.eah@gmail.com

Téléphone : 06 33 95 97 85

---

## 27. DROITS ET PROPRIÉTÉ

© 2026 EAH Conformité - EAH SPORT.

Tous droits réservés.

EAH SPORT est une solution de coaching sportif connecté développée par EAH Conformité.

Toute utilisation, reproduction ou commercialisation du code doit respecter les droits applicables et les autorisations de son propriétaire.

---

**EAH SPORT**

Votre progression. Votre programme. Votre coach.

Powered by EAH Conformité.
