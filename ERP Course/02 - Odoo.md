---
title: 02 - Odoo
tags:
  - erp
  - course
  - odoo
  - tp1
  - tp2
aliases:
  - Odoo TP1 TP2
  - Odoo et achats
---

# 02 — Odoo (TP1 + TP2)

![[Odoo Purchase Flow.excalidraw|100%]]

## 1. Odoo en bref

- ERP **modulaire** et **open source**, créé en **2002** par **Fabien Pinckaers**.
- **Community** = gratuit ; **Enterprise** = payant (Odoo Online, serveurs locaux, **Odoo.sh**).
- **Python** (modèles), **PostgreSQL** (SGBD), **XML** (vues).
- **`__manifest__.py`** = décrit un module ; **`__init__.py`** = package Python ; **`security/ir.model.access.csv`** = droits d'accès.
- **Domain** = filtre d'enregistrements. **ORM** = manipuler les données sans écrire du SQL.
- **Vue Odoo** = **interface** (pas une vue SQL).
- Personnaliser = **créer un module qui étend**, jamais modifier le code source.

## 2. Base éducative et navigation

- Préfixe **`edu-`** dans le nom → gratuit **2 ans**.
- Se connecter **tous les 3 mois** (sinon base archivée).
- Lien du prof : **`edu-Matricule-Groupe`**, pays **Tunisie**, activation **sous 3 h**.
- **Apps** = installer/désinstaller ; **Paramètres** = configurer.

## 3. Mode développeur

| Action | URL / repère |
|---|---|
| Activer | **`?debug=1`** |
| Désactiver | **`?debug=0`** |
| Front-end (assets) | **`?debug=assets`** |
| Repère | Icône **scarabée** |
| Palette de commandes | **Ctrl + K** |

## 4. Utilisateurs et droits

- Un **utilisateur** = un compte avec des **droits d'accès** (via des **groupes**).
- Un utilisateur peut être lié à **un seul employé** au plus.
- **Admin par défaut** = créateur de la base.
- Chemin : **Paramètres → Utilisateurs & Sociétés → Utilisateurs**.

## 5. Achats : produits et flux

**Flux** : Besoin → **Demande de prix (RFQ)** → **Bon de commande** → **Réception** → **Facture** → Paiement.

| Catégorie | Stocké | Compte (Tunisie) |
|---|---|---|
| **Goods** (marchandises) | Oui | **607** achats / **707** ventes |
| **Expenses** (consommables) | Non | **606** |
| **Services** (prestations) | Non | **615** |

- **Variante** = déclinaison d'un produit modèle selon des **attributs** (taille, couleur).
- **Liste de prix fournisseur** dépend de : **produit + quantité + fournisseur + période + remise**.
- Réception : **Inventaire → Réceptions → Valider** → le stock augmente.

## 6. Réapprovisionnement

> [!important] Les 2 formules
> **Stock disponible = stock réel + en commande − réservé**
>
> Si **dispo < Min** → **Quantité à commander = Max − dispo**

| Situation (Min = 5, Max = 20) | Réel | Cmd | Réservé | Dispo | Résultat |
|---|---|---|---|---|---|
| RFQ de 5 en cours | 0 | 5 | 0 | **5** | pas < 5 → **0** |
| RFQ annulée | 0 | 0 | 0 | **0** | **20** |
| 20 reçus, 18 réservés | 20 | 0 | 18 | **2** | **18** |
| 0 reçu, 18 réservés | 0 | 0 | 18 | **−18** | **38** |

## 7. Mini-test

> [!question]- Langage, SGBD, vues ?
> **Python**, **PostgreSQL**, vues **XML**.

> [!question]- Comment activer le mode développeur ?
> URL **`?debug=1`** (ou Paramètres → Outils développeur).

> [!question]- Où sont les droits d'accès d'un module ?
> **`security/ir.model.access.csv`**.

> [!question]- Comptes des 3 catégories ?
> Goods **607/707**, Expenses **606**, Services **615**.

> [!question]- Formule de la quantité à commander ?
> Si dispo < Min : **Max − dispo**, avec **dispo = réel + en commande − réservé**.
