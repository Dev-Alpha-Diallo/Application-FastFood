# Cahier des Charges – Application de Gestion de Mini Fast-Food

## 1. Présentation du Projet

L'objectif du projet est de concevoir et développer une application professionnelle permettant de gérer les activités d'un mini fast-food. L'application sera composée de deux espaces distincts :

* **Espace Gestionnaire de Vente (Caissier)**
* **Espace Propriétaire (Admin)**

Le système facilite l'enregistrement des ventes avec gestion des menus, variantes, suppléments et promotions, le suivi des activités des gestionnaires, l'impression de tickets avec numéro de commande, la gestion des utilisateurs et l'analyse des performances du fast-food. **Aucune gestion de stock n'est incluse.**

---

## 2. Objectifs du Système

* Automatiser l'enregistrement des ventes avec menus personnalisables.
* Générer les tickets client et cuisine avec numéro de commande.
* Permettre la gestion multi-caissiers avec sessions individuelles.
* Gérer les variantes de menus (tailles) et suppléments payants.
* Appliquer des promotions et réductions automatiques.
* Fournir au propriétaire une visualisation complète des ventes.
* Offrir un tableau de bord clair et moderne aux deux types d'utilisateurs.
* Enregistrer l'historique des ventes et dépenses.
* Produire des rapports journaliers, mensuels et annuels.

---

## 3. Fonctionnalités

### 3.1. Espace Gestionnaire de Vente (Caissier)

* Authentification avec identifiants personnels.
* Dashboard simple affichant : ventes du jour, dernières opérations.
* Création de ventes :
  * Sélection des **menus** (ex: Menu Burger, Menu Tacos, Menu Poulet, etc.).
  * Choix de la **variante/taille** (S, M, L, XL selon le menu).
  * Ajout de **suppléments payants** (fromage, bacon, sauce spéciale, etc.).
  * Quantités.
  * Application automatique des **promotions actives**.
  * Application manuelle de **réductions** (avec autorisation si nécessaire).
  * Calcul automatique du total avec détails.
  * Choix du mode de paiement (cash / mobile money).
  * Génération automatique du **numéro de commande**.
  * Génération automatique du ticket client.
  * Génération du ticket cuisine avec numéro de commande.
* Historique des ventes du caissier.
* Annulation d'une vente (avec justificatif).
* Enregistrement des dépenses journalières.
* Consultation du profil.

---

### 3.2. Espace Propriétaire (Admin)

* Authentification sécurisée.
* Dashboard complet affichant :
  * Ventes journalières, hebdomadaires et mensuelles.
  * Nombre de tickets/commandes.
  * Classement des **menus** les plus vendus.
  * Performance des promotions.
  * Liste des caissiers actifs.
  * Suppléments les plus demandés.
* **Gestion des menus** : 
  * Ajout, modification, suppression de menus.
  * Organisation par catégories (Burgers, Tacos, Poulet, Boissons, Desserts, etc.).
  * Définition du **prix de base** de chaque menu.
  * Configuration des **variantes/tailles** avec prix différenciés (ex: S: 2000 FCFA, M: 2500 FCFA, L: 3000 FCFA).
  * Gestion des **suppléments disponibles** par menu (ex: +fromage: 200 FCFA, +bacon: 300 FCFA).
  * Ajout d'images pour chaque menu.
  * Description et composition des menus.
  * Statut de disponibilité.
* **Gestion des suppléments** :
  * Création de suppléments globaux (fromage, sauces, extras).
  * Prix de chaque supplément.
  * Association aux menus compatibles.
* **Gestion des promotions** :
  * Création de promotions (pourcentage ou montant fixe).
  * Période de validité (date début/fin).
  * Application sur menus spécifiques ou globale.
  * Conditions d'application (ex: à partir de 2 menus).
  * Activation/désactivation.
* Gestion des caissiers : ajout, suspension, suivi de leur activité.
* Consultation des ventes :
  * Par jour, semaine, mois, année.
  * Par caissier.
  * Par menu.
  * Par numéro de commande.
* Gestion des dépenses.
* Génération de rapports exportables (PDF / Excel).
* Paramétrage de l'application :
  * Informations du fast-food.
  * Logo.
  * Paramètres des tickets.
  * Format du numéro de commande.

---

## 4. Structure des Pages

### 4.1. Côté Caissier

1. Page de Login
2. Dashboard
3. Nouvelle Vente (avec sélection menu, variantes, suppléments, promotions)
4. Ticket Client (avec numéro de commande)
5. Ticket Cuisine (avec numéro de commande et détails)
6. Historique des Ventes
7. Dépenses
8. Profil

### 4.2. Côté Propriétaire

1. Page de Login Admin
2. Dashboard Principal
3. **Gestion des Menus** (avec variantes et suppléments)
4. **Gestion des Suppléments**
5. **Gestion des Promotions**
6. Gestion des Caissiers
7. Ventes (journalières, mensuelles, annuelles)
8. Recherche de Commande (par numéro)
9. Dépenses
10. Rapports (PDF / Excel)
11. Paramètres

---

## 5. User Stories

### Pour les Gestionnaires de Vente

* En tant que caissier, je veux me connecter pour accéder à mon espace.
* En tant que caissier, je veux enregistrer une vente en sélectionnant un menu, sa taille et ses suppléments.
* En tant que caissier, je veux que les promotions s'appliquent automatiquement.
* En tant que caissier, je veux voir le numéro de commande généré automatiquement.
* En tant que caissier, je veux générer un ticket client et un ticket cuisine avec le numéro de commande.
* En tant que caissier, je veux voir l'historique de mes ventes du jour.
* En tant que caissier, je veux annuler une vente avec justificatif.
* En tant que caissier, je veux enregistrer une dépense.

### Pour le Propriétaire

* En tant que propriétaire, je veux visualiser toutes les ventes en temps réel.
* En tant que propriétaire, je veux créer/supprimer des caissiers.
* En tant que propriétaire, je veux **gérer la carte des menus** avec leurs variantes de tailles.
* En tant que propriétaire, je veux **créer des suppléments** et les associer aux menus.
* En tant que propriétaire, je veux **créer des promotions** avec dates de validité.
* En tant que propriétaire, je veux suivre la performance des caissiers.
* En tant que propriétaire, je veux rechercher une commande par son numéro.
* En tant que propriétaire, je veux afficher les ventes selon des filtres (par menu, par période).
* En tant que propriétaire, je veux consulter les dépenses.
* En tant que propriétaire, je veux exporter les rapports.
* En tant que propriétaire, je veux voir quels suppléments sont les plus populaires.
* En tant que propriétaire, je veux analyser l'impact de mes promotions.

---

## 6. Structure de la Base de Données

### Tables Principales

#### 6.1. Table `users` (Utilisateurs)
* id
* nom
* prenom
* email
* password
* role (admin / caissier)
* statut (actif / suspendu)
* created_at, updated_at

#### 6.2. Table `menus`
* id
* nom (ex: Menu Burger Classique)
* categorie_id (référence vers categories)
* description
* prix_base (prix de référence, généralement pour la taille S ou standard)
* image_url
* disponible (oui / non)
* created_at, updated_at

#### 6.3. Table `categories`
* id
* nom (Burgers, Tacos, Poulet, Boissons, Desserts)
* description
* ordre_affichage
* created_at, updated_at

#### 6.4. Table `variantes_menu` (Tailles : S, M, L, XL)
* id
* menu_id (référence vers menus)
* nom_variante (S, M, L, XL)
* prix
* disponible (oui / non)
* created_at, updated_at

#### 6.5. Table `supplements`
* id
* nom (Fromage, Bacon, Sauce Spéciale, etc.)
* prix
* disponible (oui / non)
* created_at, updated_at

#### 6.6. Table `menu_supplements` (Table pivot)
* id
* menu_id (référence vers menus)
* supplement_id (référence vers supplements)
* created_at, updated_at

#### 6.7. Table `promotions`
* id
* nom (ex: Happy Hour, Promo Week-End)
* description
* type (pourcentage / montant_fixe)
* valeur (ex: 10 pour 10%, ou 500 pour 500 FCFA de réduction)
* date_debut
* date_fin
* conditions (JSON : minimum d'achat, menus concernés, etc.)
* actif (oui / non)
* created_at, updated_at

#### 6.8. Table `ventes`
* id
* numero_commande (ex: CMD-20231215-001)
* caissier_id (référence vers users)
* montant_brut (avant réductions)
* montant_promotion (réduction appliquée)
* montant_reduction (réduction manuelle)
* montant_total (montant final)
* mode_paiement (cash / mobile money)
* statut (validée / annulée)
* justificatif_annulation
* date_vente
* created_at, updated_at

#### 6.9. Table `ligne_ventes` (Détails des ventes)
* id
* vente_id (référence vers ventes)
* menu_id (référence vers menus)
* variante_id (référence vers variantes_menu, nullable)
* quantite
* prix_unitaire_base
* prix_variante
* sous_total_menu
* created_at, updated_at

#### 6.10. Table `ligne_vente_supplements` (Suppléments commandés)
* id
* ligne_vente_id (référence vers ligne_ventes)
* supplement_id (référence vers supplements)
* quantite
* prix_unitaire
* sous_total
* created_at, updated_at

#### 6.11. Table `depenses`
* id
* caissier_id (référence vers users)
* montant
* motif
* date_depense
* created_at, updated_at

#### 6.12. Table `parametres`
* id
* nom_fast_food
* adresse
* telephone
* email
* logo_url
* format_numero_commande (ex: CMD-{date}-{increment})
* created_at, updated_at

---

## 7. Logique Métier

### 7.1. Génération du Numéro de Commande
* Format suggéré : `CMD-YYYYMMDD-XXX`
* Exemple : `CMD-20231215-001`, `CMD-20231215-002`
* Auto-incrémenté par jour
* Unique et séquentiel

### 7.2. Calcul du Prix d'une Ligne de Vente
```
Prix ligne = (Prix base menu + Prix variante + Somme des suppléments) × Quantité
```

### 7.3. Application des Promotions
* Vérification automatique des promotions actives à la date de vente
* Application selon les conditions définies
* Enregistrement du montant de la promotion appliquée
* Affichage sur le ticket

### 7.4. Calcul du Montant Total
```
Montant Total = Montant Brut - Montant Promotion - Montant Réduction Manuelle
```

---

## 8. Format des Tickets

### 8.1. Ticket Client
```
=============================
    [LOGO FAST-FOOD]
    Nom du Fast-Food
    Adresse
    Tél: XXXXXXXXX
=============================
Commande N°: CMD-20231215-042
Date: 15/12/2023 14:30
Caissier: Prénom Nom
=============================

1x Menu Burger Classique (M)
   Prix base: 2500 FCFA
   + Fromage: 200 FCFA
   + Bacon: 300 FCFA
   Sous-total: 3000 FCFA

2x Menu Tacos (L)
   Prix base: 3500 FCFA
   Sous-total: 7000 FCFA

-----------------------------
Montant Brut:      10000 FCFA
Promotion (-10%):   -1000 FCFA
-----------------------------
TOTAL À PAYER:      9000 FCFA

Mode de paiement: Cash
Monnaie rendue: 1000 FCFA

=============================
   Merci de votre visite !
   À bientôt !
=============================
```

### 8.2. Ticket Cuisine
```
=============================
    COMMANDE CUISINE
=============================
Commande N°: CMD-20231215-042
Date: 15/12/2023 14:30
Caissier: Prénom Nom
=============================

[ ] 1x Menu Burger Classique (M)
    + Fromage
    + Bacon

[ ] 2x Menu Tacos (L)

=============================
Heure impression: 14:30
=============================
```

---

## 9. Contraintes Techniques

* Application responsive (mobile, tablette, desktop).
* Backend recommandé : **Laravel 10+** (API REST).
* Application mobile : **Flutter 3+**.
* Dashboard web propriétaire : Laravel Blade ou Vue.js 3.
* Impression compatible avec imprimantes thermiques (POS) - Format 80mm.
* Sécurité renforcée (sessions, tokens JWT, rôles et permissions).
* Base de données : **MySQL 8+** ou **PostgreSQL 14+**.
* Système de cache pour améliorer les performances (Redis recommandé).
* Validation stricte des données côté backend.
* Logs détaillés des actions sensibles (annulations, modifications).

---

## 10. Livrables

* Architecture technique complète avec diagrammes UML.
* Base de données fonctionnelle avec schéma relationnel détaillé.
* API REST sécurisée avec documentation Swagger/OpenAPI.
* Application mobile Flutter (Android + iOS).
* Interface web propriétaire responsive.
* Module d'impression thermique.
* Documentation utilisateur complète (caissier + propriétaire).
* Documentation technique (API, déploiement, maintenance).
* Rapports PDF/Excel configurables.
* Guide d'installation et de déploiement.
* Scripts de migration et seed de données de test.

---

## 11. Phases de Développement

### Phase 1 : Conception (2 semaines)
- Validation du cahier des charges
- Conception de la base de données
- Maquettes UI/UX (Figma)
- Architecture technique

### Phase 2 : Backend (4 semaines)
- Configuration Laravel
- Développement de l'API REST
- Authentification JWT
- Gestion des menus, variantes, suppléments
- Système de promotions
- Génération des numéros de commande
- Tests unitaires

### Phase 3 : Frontend Caissier (3 semaines)
- Application Flutter
- Interface de vente
- Gestion des variantes et suppléments
- Module d'impression
- Tests utilisateurs

### Phase 4 : Frontend Propriétaire (3 semaines)
- Interface web d'administration
- Dashboard analytics
- Gestion complète des menus
- Gestion des promotions
- Génération de rapports

### Phase 5 : Tests et Déploiement (2 semaines)
- Tests d'intégration
- Tests de charge
- Correction de bugs
- Déploiement
- Formation des utilisateurs

---

## 12. Points Validés

### ✅ Fonctionnalités confirmées
- [x] Gestion des **variantes/tailles** de menus (S, M, L, XL)
- [x] Gestion des **suppléments payants** (fromage, bacon, etc.)
- [x] Système de **promotions et réductions**
- [x] Seul le **propriétaire** peut gérer les menus
- [x] **Numéro de commande** unique pour chaque vente

### ✅ Technologies validées
- [x] Backend Laravel
- [x] Mobile Flutter
- [x] Base de données MySQL/PostgreSQL
- [x] Authentification JWT

### ✅ Périmètre du projet
- [x] Pas de gestion de stock
- [x] Pas de gestion des ingrédients
- [x] Pas de système de fidélité client
- [x] Pas de réservations
- [x] Impression thermique pour tickets

---

## 13. Conclusion

Ce cahier de charges définit de manière complète et détaillée les besoins fonctionnels et techniques de l'application de gestion de fast-food. Le système offre une solution professionnelle complète avec :

* Gestion flexible des menus avec variantes et suppléments
* Système de promotions automatisé
* Numérotation des commandes pour un suivi optimal
* Interface intuitive pour les caissiers
* Outils d'analyse puissants pour le propriétaire

L'application garantit une meilleure efficacité opérationnelle, une transparence totale des ventes et un contrôle précis des performances du fast-food.
