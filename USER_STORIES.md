# User Stories - Plateforme

## Contexte
Botiga est une plateforme pour dynamiser le commerce local, permettant aux utilisateurs de découvrir et d'interagir avec les commerces de proximités.

## Les profils utilisateurs
- Visiteur → peut créer un compte
- Utilisateur standard → peut consulter, noter, commenter, mettre en favoris.
- Commerçant / artisan (admin) → crée un compte, gère fiches, promos, événements, collaborateurs.
- Collaborateur commerçant / artisan → agit dans le périmètre défini par Commerçant / artisan (admin).
- Administration → valide, modère, supervise, analyse.

Note : 
- Chaque commerçant/artisan est rattaché à un compte principal (administrateur), qui peut créer des profils collaborateurs disposant de permissions limitées.
- Les données personnelles sont sauvegardées et traitées conformément au RGPD.
- L'administration est le gestionnaire de la plateforme.

========================================================================
## 1. Gestion des utilisateurs

### US001 - Inscription d'un nouvel utilisateur
**En tant que** visiteur
**Je veux** créer un compte sur la plateforme
**Afin de** pouvoir accéder aux fonctionnalités de la page

**Critères d'acceptation :**
- Je peux saisir mon nom, email et mot de passe.
- Un message d’erreur clair s’affiche en cas de saisie invalide (email, mot de passe).
- Mon email doit être au format valide et ne pas être déjà utilisé.
- Un message d’erreur s’affiche si l’email est déjà enregistré.
- Mon mot de passe doit contenir au moins 6 caractères.
- Je reçois une confirmation après inscription réussie.
- Mon compte est créé avec un profil vide à compléter plus tard.
- Je dois donner mon consentement explicite pour le traitement des données.

### US002 - Connexion à la plateforme
**En tant qu'** utilisateur enregistré (tous profils confondus)
**Je veux** me connecter à mon compte
**Afin d'** accéder à mes fonctionnalités personnalisées

**Critères d'acceptation :**
- Je peux me connecter avec mon email et mon mot de passe.
- Un message d’erreur clair s’affiche en cas de saisie invalide (email, mot de passe).
- Je reçois un token d'authentification.
- Je suis redirigé vers mon tableau de bord adapté à mon rôle (utilisateur, commerçant, collaborateur, administration).
- Un message d'erreur s'affiche en cas d'identifiants incorrects.

### US003 - Gestion de mon profil utilisateur standard
**En tant qu'** utilisateur standard connecté
**Je veux** créer et modifier mon profil
**Afin de** personnaliser mon expérience et faciliter mes interactions

**Critères d'acceptation :**
- Je peux renseigner mon adresse complète (rue, ville, code postal) 
- Je peux ajouter mon numéro de téléphone.
- Je peux modifier mon mot de passe à tout moment.
- Je peux configurer mes informations de paiement.
- Je peux modifier ces informations à tout moment.
- Mes informations sont sauvegardées de manière sécurisée.
- Je dois avoir la possibilité de supprimer mon compte.

========================================================================
## 2. Découverte des Commerces

### US004 - Recherche de commerces locaux
**En tant qu'** utilisateur standard
**Je veux** rechercher des commerces près de chez moi
**Afin de** découvrir l'offre commerciale locale

**Critères d'acceptation :**
- Je peux rechercher par type de commerce (catégorie ou mot-clé).
- Je peux filtrer par distance géographique.
- Je peux afficher les commerces sur une carte interactive.
- Je peux autoriser ou refuser la géolocalisation.
- Si je refuse, je peux saisir manuellement ma localisation.
- Je peux visualiser l'itinéraire pour me rendre au commerce.
- Je peux contacter le commerce.
- Les résultats affichent les informations essentielles (nom, adresse, horaires, contact).
- Les résultats sont triés par pertinence ou distance.
- Un message s’affiche s’il n’y a aucun commerce trouvé.

### US005 - Consultation des détails d'un commerce
**En tant qu'** utilisateur standard
**Je veux** consulter des informations détaillées d'un commerce
**Afin de** prendre une décision éclairée

**Critères d'acceptation :**
- Je peux voir les horaires d'ouvertures.
- Je peux consulter les produits/services.
- Je peux voir les avis et notes des autres utilisateurs.
- Je peux obtenir l'itinéraire vers le commerce.

========================================================================
## 3. Interaction avec les commerces

### US006 - Évaluation et avis sur un commerce
**En tant qu'** utilisateur connecté
**Je veux** laisser un avis sur un commerce
**Afin de** partager mon expérience avec la communauté

**Critères d'acceptation :**
- Je peux attribuer une note (étoiles).
- Je peux rédiger un commentaire textuel.
- Mon avis est visible par les autres utilisateurs.
- Je peux modifier ou supprimer mon avis et ma note.
- Je ne peux pas noter deux fois le même commerce.
- Je peux signaler un avis inapproprié à la modération.

### US007 - Ajout de commerce aux favoris
**En tant qu'** utilisateur connecté
**Je veux** marquer des commerces comme favoris
**Afin de** les retrouver facilement

**Critères d'acceptation :**
- Je peux ajouter/retirer un commerce de mes favoris.
- Je peux accéder à ma liste de favoris.
- Je peux filtrer mes favoris.
- Je suis notifié des actualités de mes commerces favoris.

### US008 - Commande et panier
**En tant qu'** utilisateur connecté
**Je veux** ajouter des produits à un panier
**Afin de** pouvoir acheter facilement des produits auprès des commerces locaux sur la plateforme Botiga

**Critères d'acceptation :**
- Je peux ajouter un produit/service au panier depuis la fiche d’un commerce.
- Je peux constituer un panier de produits.
- Je peux mettre un produit en favoris depuis la fiche ou le panier.

- Je peux modifier la quantité d’un produit.
- Je peux retirer un produit du panier.
- Je peux vider entièrement mon panier.
- Le montant total s’actualise automatiquement en cas de modification.
- Je peux accéder à mon panier depuis n’importe quelle page (icône visible en permanence).
- Je peux passer à la phase de commande depuis mon panier.

- Je peux choisir le mode de retrait/livraison proposé par le commerçant : retrait en magasin, livraison locale (si activée par le commerçant)

- Je peux voir un récapitulatif de ma commande : nom du produit, quantité sélectionnée, prix unitaire et total, nom du commerce associé.
- Je veux suivre l'état d'avancement de ma commande.
- Je reçois une notification lors d’un changement de statut de ma commande.
- Je peux annuler ma commande.
- Je veux consulter l'historique de mes commandes.

- Je veux pouvoir recommander un produit présent dans mon historique de commande.

### US009 - Paiement 
**En tant qu'** utilisateur connecté
**Je veux** payer des produits de mon panier et finaliser un achat en ligne de manière sécurisée
**Afin de** pouvoir acheter facilement des produits auprès des commerces locaux sur la plateforme Botiga

**Critères d'acceptation :**

- Je peux choisir mon mode de paiement : Carte bancaire (via Stripe, PayPal...)
- Je dois valider mes informations de contact et d’adresse avant paiement.
- Je reçois une confirmation de commande par email après paiement réussi.
- En cas d’échec du paiement, un message d’erreur clair s’affiche.
- Les données bancaires sont stockées sur la plateforme Botiga de façon anonyme.
- Les transactions sont chiffrées (HTTPS + normes PCI DSS).
- Je peux consulter l'historique des paiements.
- Je peux demander un remboursement en cas d'annulation de la commande.
- Je peux payer en ligne via une solution de paiement sécurisée (comme Stripe ou PayPal Sandbox pour
l'entraînement).
- Je dois valider les conditions générales de vente (CGV) avant le paiement.

### US010 - Promotion
**En tant qu'** utilisateur connecté
**Je veux** être tenu informé des promotions
**Afin de** profiter des réductions sur mes produits favoris

**Critères d'acceptation :**
- Je peux voir sur la plateforme les promotions.
- Je peux consulter les produits promus.
- Je peux voir la différence de prix avant/après.
(BONUS- Je peux ajouter un code PROMO)

### US011 - Évènement
**En tant qu'** utilisateur connecté
**Je veux** participer à un évènement
**Afin de** participer à la vie locale et découvrir de nouveaux commerces.

**Critères d'acceptation :**
- Je peux m'inscrire à un évènement.

### US012 - Réservation
**En tant qu'** utilisateur connecté
**Je veux** réserver un produit ou service proposé par un commerçant
**Afin de** planifier un retrait ou une livraison à une date ultérieure

**Critères d'acceptation :**
- Je peux réserver un produit/service/évènement, si le service a été activé par le commerçant.
- Je peux modifier ou annuler la réservation.
- Je peux sélectionner un créneau horaire proposé par le commerçant.
- Je peux choisir le jour et l’heure du retrait ou de la livraison.
- Je peux modifier ou annuler ma réservation avant la date limite fixée.
- Je reçois une notification de confirmation ou d’annulation de ma réservation.

========================================================================
## 4. Gestion des commerces (commerçants ou artisans)

### US013 - Création d'un compte commerçant/artisan
**En tant que** commerçant ou artisan (administrateur de compte)
**Je veux** créer un compte professionnel sur la plateforme
**Afin de** pouvoir accéder aux fonctionnalités dédiées à la gestion de mon commerce

**Critères d'acceptation :**
- Un compte commerçant doit avoir un seul numéro de SIRET.
- Saisir le nom de ma société, l'adresse du siège social, le numéro de SIRET de ma société, mon nom, ma fonction, mon email, mon numéro de téléphone et mon mot de passe.
- Mon email doit être au format valide et ne pas être déjà utilisé.
- Un message d’erreur clair s’affiche en cas de saisie invalide (email, téléphone, mot de passe).
- Un message d’erreur s’affiche si l’email est déjà enregistré.
- Mon numéro de SIRET soit valide.
- Mon numéro de téléphone est valide.
- Mon mot de passe doit contenir au moins 6 caractères.
- Je reçois un email de confirmation lorsque mon compte est validé par l’administration.
- Tant que le compte n’est pas validé, je ne peux pas publier de contenu.
- Mon compte est créé avec un profil complété.
- Je dois donner mon consentement explicite pour le traitement des données.

### US014 - Gestion de mon profil commerçant ou artisan (administrateur de compte)
**En tant qu'** commerçant ou artisan (administrateur de compte)
**Je veux** modifier mon profil
**Afin de** rester joignable et faciliter mon expérience

**Critères d'acceptation :**
- Je peux modifier mon nom, ma fonction, mon email, mon numéro de téléphone et mon mot de passe.
- Je peux modifier ces informations à tout moment.
- Un message de confirmation s’affiche après chaque mise à jour réussie.
- Je peux supprimer mon compte à tout moment.

<!--BONUS  
### US - Création et gestion de profils collaborateurs
**En tant que** commerçant ou artisan (administrateur de compte) enregistré
**Je veux** créer et gérer les profils collaborateurs associés à mon commerce
**Afin de** déléguer certaines tâches à mes collaborateurs

**Critères d'acceptation :**
- Mon compte commerçant ou artisan (administrateur de compte) validé par l’administration.
- Saisir le nom, la fonction, le mail du collaborateur.
- Je reçois une confirmation après ajout d'un profil réussi.
- Mon collaborateur reçoit par mail une demande de connexion afin de définir son mot de passe dans les 24h.
- Je peux ajouter, désactiver ou supprimer un profil collaborateur.
- Je peux attribuer des permissions spécifiques (ex : gestion fiches, événements, promotions).
- Les informations sont sauvegardées de manière sécurisée.
- Les collaborateurs doivent donner leur consentement explicite pour le traitement des données.
- Les collaborateurs doivent avoir la possibilité de supprimer leur profil.
-->

### US015 - Gestion de mon profil collaborateur
**En tant qu'** collaborateur commerçants / artisans connecté
**Je veux** compléter et modifier mon profil personnel
**Afin de** personnaliser mon expérience et faciliter mes interactions dans le cadre du commerce auquel je suis rattaché

**Critères d'acceptation :**
- Je peux consulter et modifier mes informations personnelles (nom, prénom, fonction, numéro de téléphone, email professionnel).
- Je peux modifier mon mot de passe à tout moment.
- Je peux ajouter mon numéro de téléphone.
- Je peux modifier ces informations à tout moment.
- Mes informations sont sauvegardées de manière sécurisée conformément au RGPD.

### US016 - Création et gestion d’une fiche de commerce et des produits/services associés avec vente en ligne
**En tant que** commerçants ou artisans enregistrés
**Je veux** créer et gérer une fiche de commerce et des produits/services associés
**Afin de** rendre visible mon offre de produits/services et permettre aux utilisateurs d’acheter directement sur la plateforme

**Critères d'acceptation :**
- Mon compte commerçant ou artisan (administrateur de compte) doit être validé par l’administration.
- Je peux ajouter le nom du commerce, une description, les horaires d’ouverture, l’adresse, et un contact (SAV, demande d’information).
- Je peux mettre à jour ou supprimer une fiche de commerce.

- Je peux ajouter des produits ou services à ma fiche avec les informations suivantes : nom du produit / service, description, prix TTC, stock disponible, photo, catégorie.
- Je peux activer ou désactiver la vente en ligne pour chaque produit.
- Je peux modifier ou supprimer un produit/service.
- Je peux gérer une promotion.
- Je peux sauvegarder une fiche en brouillon avant de la publier.
- Les images des produits sont redimensionnées et optimisées automatiquement.

- Le panier affiche : nom du produit, prix unitaire, quantité, total.
- Je peux définir mes modes de livraison ou retrait : Retrait en boutique, Livraison locale (si disponible)
- Je reçois une notification lors d’une nouvelle commande.

- Je peux gérer le statut des commandes (en attente, en cours, livrée, annulée).
- Je peux consulter l’historique des ventes sur mon tableau de bord.
- Je peux télécharger les factures émises.

- Je peux visualiser les statistiques de mes ventes sous forme de tableau et graphique (nombre d’utilisateurs et commerces actifs, nombre de vues par produit/service, nombre de commandes, taux de conversion)
- Je peux extraire mes données de statistiques de ventes sous format .pdf ou .xls

- Je peux gérer les stocks.

<!-- BONUS 
### US - Gestion des avoirs
**En tant que** commerçants ou artisans enregistrés
**Je veux** 
**Afin de**
-->

### US017 - Réservation chez un commerçant
**En tant que** commerçants ou artisans enregistrés
**Je veux** permettre à l'utilisateur de réserver en ligne
**Afin de** gérer mon planning

**Critères d'acceptation :**
- Je peux activer la réservation en ligne pour mon commerce.
- Je peux définir les créneaux horaires disponibles.
- Je peux configurer la durée des créneaux pour la réservation (15min, 30min, 1h).
- Je peux définir la date limite de réservation (dans le cadre d'un évènement).
- Je peux définir le nombre de place sur un créneau.
- Je suis notifié d'une réservation.
- Je peux confirmer, supprimer, modifier une réservation.
- Je peux consulter mon planning.

### US018 - Création d'un évènement
**En tant que** commerçants ou artisans enregistrés
**Je veux** créer un évènement
**Afin de** rendre visible mon évènement et rediriger vers la réservation 

**Critères d'acceptation :**
- Mon compte commerçant ou artisan (administrateur de compte) validé par l’administration.
- Je peux ajouter le nom de mon évènement, la description, photos, la date.

### US019 - Gestion des évènements
**En tant que** commerçants ou artisans enregistrés
**Je veux** gérer un évènement
**Afin de** mettre à jour mes évènements

**Critères d'acceptation :**
- Je peux modifier le nom de mon évènement, la description, des photos, la date, le lieu.
- Je peux supprimer un évènement.

### US020 - Création d'une promotion
**En tant que** commerçants ou artisans enregistrés
**Je veux** créer une promotion
**Afin de** rendre visible ma promotion

**Critères d'acceptation :**
- Mon compte commerçant ou artisan (administrateur de compte) validé par l’administration.
- Je peux ajouter le nom du produit ou service en promotion, le prix avant/après, une brève description du produit et une photo.

### US021 - Gestion des promotions
**En tant que** commerçants ou artisans enregistrés
**Je veux** gérer une promotion
**Afin de** mettre à jour mes promotions

**Critères d'acceptation :**
- Je peux créer une campagne promotionnelle (texte, image, lien)
- Je peux supprimer une promotion.
- Je peux envoyer des messages ou des promotions aux utilisateurs ayant mis en favoris mon commerce ou mes produits/services afin de fidéliser ma clientèle.

### US022 - Gestion des avis déposés par les clients
**En tant qu'** commerçants ou artisans enregistrés
**Je veux** gérer les avis clients
**Afin de** gérer ma réputation et améliorer mes services.

**Critères d'acceptation :**
- Je peux voir les avis et notes attribués sur mes produits et services.
- Je veux répondre ou signaler les avis laissés sur mon commerce.

==================================================================
## 5. Gestion de la plateforme Botiga

### US023 - Validation des comptes des commerçants/artisans
**En tant qu'** administration
**Je veux** valider un compte commerçant sur la plateforme
**Afin de** rendre fiable la plateforme

**Critères d'acceptation :**
- Je vérifie le nom de la société, l'adresse du siège social, le numéro de SIRET de la société.
- Je peux notifier par mail au commerçant/artisan la validation ou non de son compte en mentionnant les motifs.

### US024 - Modération des contenus publiés
**En tant qu'** administration
**Je veux** refuser ou supprimer toutes publications non conformes
**Afin de** faire respecter la règlementation en vigueur et les conditions générales d'utilisation de la plateforme

**Critères d'acceptation :**
- Je peux visualiser les contenus publiés ou en attente de validation.
- Je peux valider, refuser ou supprimer un contenu.
- Je dois pouvoir indiquer le motif d'un refus avant l’envoi d’une notification.
- Je peux notifier par mail au commerçant/artisan ou visiteur le refus ou la suppression d'un contenu.
- Je peux consulter les signalements (réclamation).
- Je peux supprimer ou masquer des contenus inappropriés.
- Je peux suspendre des comptes utilisateurs.
- Je peux supprimer des comptes utilisateurs.

### US025 - Gestion des statistiques
**En tant qu'** administration
**Je veux** accéder à des statistiques sur les ventes
**Afin de** publier les résultats aux commerçants/artisans locaux

**Critères d'acceptation :**
- Je peux filtrer par type de commerce les statistiques globales.
- Je peux voir le nombre d’utilisateurs et commerces actifs.
- Je peux extraire mes données de statistiques de ventes sous format .xls
- Je peux générer un rapport d'activité sous format .pdf

<!-- Maquetter en WireFriming :

Faire dans un premier temps
Gestion des utilisateurs
Gestion des commerces
Découverte des commerces

Faire en second
Commande
Paiement
Réservation

Faire en troisième
Fidélité 
Statistique
Administration 

Page Accueil
Page Profil :
    modifier des infos
    consulter commande
    paiement
        Page commande
        Page paiement

Page formulaire de connexion
Page formulaire d'inscription

Pour chaque page créée, mettre le numéro US associé.
-->