---
title: 04 - QCM
tags:
  - erp
  - course
  - qcm
aliases:
  - QCM ERP
  - QCM Odoo
---

# 04 — QCM (théorie + Odoo)

> [!tip] Mode d'emploi
> Réponds sans regarder, puis vérifie dans le **corrigé** en bas. Objectif : **≥ 20/24**.

## A. Théorie

**1.** Quelle est la définition principale d'un ERP ?
- a) Un logiciel de comptabilité simple.
- b) Un progiciel de gestion intégré qui centralise l'information de l'entreprise.
- c) Un outil de gestion de projet.
- d) Un système de gestion des stocks.

**2.** Quel est l'objectif principal d'un ERP ?
- a) Augmenter les coûts.
- b) Relier les informations de l'entreprise via une base de données commune.
- c) Complexifier les processus.
- d) Isoler les fonctions.

**3.** Quelles sont les caractéristiques principales d'un ERP ?
- a) Bases multiples, faible paramétrage.
- b) Base unique, intégration de la gestion, paramétrage poussé.
- c) Architecture fermée, outils limités.
- d) Fonctionnalités indépendantes, sans paramétrage.

**4.** Quelle est l'origine de l'ERP ?
- a) Le Cloud Computing.
- b) Une évolution du MRP2.
- c) Un logiciel RH.
- d) Un outil CRM.

**5.** Qu'est-ce qu'un processus ?
- a) La manière de mettre en œuvre une activité.
- b) Un enchaînement d'activités réalisées par des acteurs.
- c) Un outil de reporting.
- d) L'organigramme de l'entreprise.

**6.** Qu'est-ce qu'une procédure ?
- a) Un ensemble d'activités transversales.
- b) La définition du « quoi faire ».
- c) La manière de mettre en œuvre un processus.
- d) Un flux automatisé.

**7.** Qu'est-ce que le workflow ?
- a) Un outil de reporting.
- b) Un processus d'achat.
- c) L'automatisation d'un processus métier.
- d) Une interface de base de données.

**8.** Quel est l'avantage principal d'un ERP Cloud ?
- a) Il faut acheter des serveurs.
- b) Faible mobilité.
- c) Accès à distance via Internet avec réduction des coûts d'infrastructure.
- d) Limité à un seul utilisateur.

**9.** Qu'est-ce qu'un module horizontal ?
- a) Spécifique à un secteur.
- b) Commun à toutes les entreprises (GRH, finance).
- c) Gestion de la production.
- d) E-commerce.

**10.** Qu'est-ce qu'un module vertical ?
- a) Commun à toutes les entreprises.
- b) Spécifique aux entreprises d'un même secteur.
- c) Gestion des achats.
- d) Reporting financier.

**11.** Qu'est-ce que la licence GPL ?
- a) Modifier sans partager.
- b) Redistribuer le programme avec ses sources complètes.
- c) Réservée aux ERP propriétaires.
- d) Permet des dérivés propriétaires.

**12.** Quels sont les principaux types de processus ?
- a) Vente, marketing, distribution.
- b) Opérationnels, support, pilotage.
- c) Comptables, financiers, RH.
- d) Achat, production, livraison.

## B. Odoo

**13.** Qu'est-ce qu'Odoo ?
- a) Un système d'exploitation.
- b) Un ERP.
- c) Un antivirus.
- d) Un navigateur.

**14.** Quel menu permet d'installer des applications ?
- a) Ventes.
- b) Contacts.
- c) Applications (Apps).
- d) Calendrier.

**15.** Langage principal des modèles Odoo ?
- a) Python.
- b) Java.
- c) C++.
- d) PHP.

**16.** Quel SGBD utilise Odoo ?
- a) MySQL.
- b) SQLite.
- c) PostgreSQL.
- d) MongoDB.

**17.** Les vues Odoo sont définies en…
- a) XML.
- b) SQL.
- c) C++.
- d) Bash.

**18.** Où trouve-t-on les droits d'accès d'un module ?
- a) `security/ir.model.access.csv`.
- b) `access/security.py`.
- c) `rights.xml`.
- d) `users.csv`.

**19.** Quel fichier décrit un module Odoo ?
- a) `__manifest__.py`.
- b) `manifest.xml`.
- c) `module.json`.
- d) `config.py`.

**20.** Le domain sert à…
- a) Filtrer des enregistrements.
- b) Créer une base.
- c) Modifier Python.
- d) Installer un module.

**21.** Une vue Odoo concerne…
- a) L'interface et la présentation des données.
- b) La structure de stockage en base (vue SQL).

**22.** Pour personnaliser un module existant, il faut…
- a) Modifier le code source original.
- b) Créer un module qui étend l'existant.
- c) Modifier PostgreSQL.
- d) Supprimer le module.

**23.** Quelle URL active le mode développeur ?
- a) `?test=1`.
- b) `?debug=1`.
- c) `?dev=true`.
- d) `?mode=developer`.

**24.** Que fait `?debug=assets` ?
- a) Efface les données de test.
- b) Débogue le front-end (JS/CSS/vues).
- c) Réservé à Enterprise.
- d) Aucune différence.

## Corrigé

| Q | Rép. | Pourquoi |
|---|---|---|
| 1 | **b** | Un ERP centralise via un PGI. |
| 2 | **b** | Base de données **commune**. |
| 3 | **b** | Base unique + intégration + paramétrage. |
| 4 | **b** | Évolution du **MRP2**. |
| 5 | **b** | Enchaînement d'activités. |
| 6 | **c** | Procédure = « comment faire ». |
| 7 | **c** | Automatisation d'un processus. |
| 8 | **c** | Accès distant + moins d'infra. |
| 9 | **b** | Horizontal = tous secteurs. |
| 10 | **b** | Vertical = un secteur. |
| 11 | **b** | GPL = sources complètes. |
| 12 | **b** | Opérationnels / support / pilotage. |
| 13 | **b** | Odoo est un ERP. |
| 14 | **c** | Apps installe les modules. |
| 15 | **a** | Python. |
| 16 | **c** | PostgreSQL. |
| 17 | **a** | XML. |
| 18 | **a** | `security/ir.model.access.csv`. |
| 19 | **a** | `__manifest__.py`. |
| 20 | **a** | Domain = filtre. |
| 21 | **a** | Vue Odoo = interface. |
| 22 | **b** | On étend, on ne modifie pas. |
| 23 | **b** | `?debug=1`. |
| 24 | **b** | Débogage front-end. |
