---
title: 01 - Theorie ERP
tags:
  - erp
  - course
  - theorie
aliases:
  - Théorie ERP
  - Fondamentaux ERP
---

# 01 — Théorie ERP

## 1. Définitions

- ==**SI**== : collecter, stocker, traiter et diffuser l'information pour soutenir la gestion et la décision.
- ==**Système informatique**== : partie matérielle + logiciels du SI.
- ==**Processus métier**== : enchaînement **transversal** d'activités qui produit un résultat à valeur ajoutée.
- ==**Procédure**== : la **manière** de mettre en œuvre un processus (« comment faire »).
- ==**Workflow**== : **automatisation** d'un processus métier.
- ==**ERP / PGI**== : application métier à **modules interconnectés**, sur une **base de données unique et partagée**, pour centraliser, standardiser et automatiser les processus.
- ==**Paramétrage**== : adapter l'ERP **sans modifier le code source**.
- ==**Traçabilité**== : retrouver l'origine de chaque information → facilite l'**audit**.

## 2. Avec vs sans ERP

| Sans ERP (vertical) | Avec ERP (transversal) |
|---|---|
| Chaque service a son logiciel + sa base | Modules interconnectés, base unique |
| Redondance, saisies multiples | Saisie unique |
| Vision partielle | Vision globale, temps réel |
| Beaucoup d'interfaces | Workflow |

![[With vs Without ERP.excalidraw|100%]]

## 3. Avantages et risques

| 5 avantages                    | 5 risques                     |
| ------------------------------ | ----------------------------- |
| Cohérence et fiabilité         | Dépendance à l'éditeur        |
| Pas de redondance              | Sécurité des données          |
| Vision globale / temps réel    | Panne = entreprise paralysée  |
| Automatisation / gain de temps | Surcoût des personnalisations |
| Traçabilité / reporting        | Résistance au changement      |

## 4. Modes de déploiement

| | Sur site | Web sur site | Cloud |
|---|---|---|---|
| Hébergement | Entreprise | Entreprise | Fournisseur |
| Accès | Réseau local | Navigateur | Internet |
| Contrôle des données | Total | Total | Limité |
| Coût initial | Élevé | Élevé | Faible |
| Mises à jour | Complexes | Centralisées | Automatiques |
| Risque principal | Coût / maintenance | Failles web | Internet / confidentialité |

- **Hybride** = une partie sur site + une partie cloud.
- **Sur site** = architecture **3 niveaux** : présentation → applicatif → données.

![[ERP Deployment Models.excalidraw|100%]]

## 5. Classements et historique

- **Généraliste** (SAP, Oracle) / **spécialisé** (Infor, CliniSys).
- **Propriétaire** (SAP, NetSuite) / **open source** (Odoo, Open-Prod).
- **GPL** = redistribution avec les **sources complètes**.
- Historique : **Gartner 1990** → **SAP R/3 1992** → Web 2000 → Cloud 2010 → Hybride 2020.
- Origine technique : **MRP** puis **MRP2**.

## 6. Mini-test

> [!question]- À quoi reconnaît-on un ERP ?
> Modules **interconnectés** + **base de données unique et partagée**.

> [!question]- Processus ou procédure ?
> **Processus** = « quoi faire » (enchaînement) ; **procédure** = « comment faire ».

> [!question]- Que fait le workflow ?
> Il **automatise** un processus métier (les modules se passent l'information).

> [!question]- Sur site ou cloud pour des données très sensibles ?
> **Sur site** (contrôle total, sécurité), au prix de coûts et de maintenance élevés.

> [!question]- Cite 3 avantages et 3 risques.
> Avantages : cohérence, vision globale, automatisation. Risques : dépendance éditeur, sécurité, panne totale.
