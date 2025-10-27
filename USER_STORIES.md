# User Stories - Plateforme

## Contexte
Botiga est une plateforme pour dynamiser le commerce local, permettant aux utilisateurs de découvrir et d'intérargir avec les commerces de proximités.

## 1. Gestion des utilisateurs
### US00I - Inscription d'un nouvel utilisateur
**En tant que** visiteur
*Je veux* créer un compte sur la plateforme

**Critères d' acceptation**
- Je peux saisir mon nom, email et mot de passe
- Mon email soit valide et unique.
- Mon mot de passe doit contenir au moins 6 caractères.
- Je reçois une confirmation après inscription réussie.
- Mon compte est crée avec un profil vide à compléter plus tard

### US002 - Connexion à la plateforme
**En tant qu'** utilisateur enregistré
**Je Veux** me connecter à mon compte
**Afin d'** accéder à mes fonctionnalités personnalisées

**Critères d t acceptation :**
- Je peux me connecter avec mon email et mon mot de passe
- Je reçois un token d'authentification
- Je suis redirigé vers mon tableau de bord
- Un message d'erreur s'affiche en cas d'identifiants incorrects