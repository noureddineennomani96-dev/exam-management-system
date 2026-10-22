# 📝 Gestion des Examens 6AP

Application web de gestion informatisée des examens de la 6ème Année Primaire (6AP)
pour la Direction Provinciale de l'Éducation Nationale d'Ouarzazate.

> Projet de stage technique – DUT Gestion des Réseaux & Sécurité  
> École Supérieure de Technologie d'Ouarzazate – Université Ibn Zohr (2025/2026)

## 🎯 Objectif

Remplacer les procédures manuelles (Excel/Word) par un système centralisé,
rapide et bilingue (arabe/français) pour gérer environ 3 500 élèves
répartis sur 113 écoles et 15 centres d'examen.

## ✨ Fonctionnalités

- 🔐 Authentification à deux profils : Administrateur et École
- 🔑 Changement obligatoire du mot de passe à la première connexion
- 📥 Import des listes d'élèves depuis un fichier Excel multi-écoles
- 🔍 Détection des doublons (empreinte MD5 du fichier + codes Massar)
- 🎲 Génération de numéros de table uniques NE-XXXX (algorithme de Fisher-Yates)
- 📅 Gestion des examens (CRUD)
- 🖨️ Génération de 4 documents officiels en PDF :
  - Convocations individuelles avec QR code
  - Étiquettes de table (grille 4×4)
  - Feuilles de présence
  - Listes des tables par salle
- ⚡ Cache des PDF générés
- 🌍 Interface bilingue avec support RTL

## 🛠️ Technologies

| Catégorie | Outils |
|---|---|
| Backend | PHP 7.4+ (sans framework) |
| Stockage | Fichiers JSON |
| Frontend | HTML5, CSS3, JavaScript (Vanilla) |
| Excel | SimpleXLSX |
| PDF | DOMPDF |
| QR Code | API QR Server |
| Environnement | XAMPP, VS Code, Git |

## 📁 Structure des données

| Fichier | Rôle |
|---|---|
| `examens.json` | Planning des examens |
| `ecoles_reference.json` | Catalogue des 113 écoles |
| `{code_ecole}_eleves.json` | Élèves d'une école avec leurs numéros NE-XXXX |
| `import_snapshot.json` | État du dernier import (MD5, date, lignes) |

## 🚀 Installation

1. Installer [XAMPP](https://www.apachefriends.org/)
2. Cloner le dépôt dans le dossier `htdocs` :
```bash
   cd C:/xampp/htdocs
   git clone https://github.com/<ton-utilisateur>/gestion-examens-6ap.git gestionExamens
```
3. Installer les dépendances (si Composer est utilisé) :
```bash
   composer install
```
4. Démarrer Apache dans XAMPP
5. Ouvrir : `http://localhost/gestionExamens/index.php`

## 🔒 Sécurité

> ⚠️ Changer le mot de passe par défaut dès la première connexion.
> Ne jamais publier de vrais identifiants ni de données d'élèves sur GitHub.
> Ajouter le dossier des données JSON au `.gitignore`.

## 📸 Captures d'écran

*(Ajouter ici les captures : connexion, dashboard, import, impression…)*

## 🔭 Perspectives

- API REST
- Application mobile pour les surveillants
- Module de saisie des résultats
- Tableau de bord statistique
- Extension à d'autres niveaux (3AC, Baccalauréat)

## 👤 Auteur

**ENNOMANI Noureddine**  
DUT Gestion des Réseaux & Sécurité – EST Ouarzazate  
Encadrant pédagogique : Mr. OUKHATAR Ayoub  
Encadrant professionnel : Mr. BAHAJ Mohamed

## 📄 Licence

Projet académique – tous droits réservés (ou choisir une licence, ex. MIT).
