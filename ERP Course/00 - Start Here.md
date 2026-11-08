---
title: ERP - Start Here
tags:
  - erp
  - course
  - moc
aliases:
  - ERP Start Here
  - Réviser ERP
---

# ERP — réviser en 1 jour

> [!tip] Objectif
> Savoir : les **définitions**, la différence **avec/sans ERP**, les **modes de déploiement**, **Odoo**, le **processus achat**, les **formules de réappro** et un **trigger**. Le reste est secondaire.

## Le plan

| Temps | Bloc | Note |
|---|---|---|
| **45 min** | Théorie ERP | [[01 - Theorie ERP]] |
| **45 min** | Odoo (TP1) | [[02 - Odoo]] |
| **60 min** | Achats + réappro (TP2) | [[02 - Odoo]] §5–6 |
| **60 min** | PL/SQL + triggers | [[03 - PL-SQL Triggers]] |
| **60 min** | QCM | [[04 - QCM]] |
| **30 min** | Fiche finale | [[05 - Cheat Sheet]] |

## Les 10 choses à savoir

1. **ERP/PGI** = modules interconnectés + **base de données unique et partagée**.
2. **Sans ERP** = vertical (silos) ; **avec ERP** = transversal (workflow).
3. **Processus** = quoi faire ; **procédure** = comment faire.
4. **Workflow** = automatisation d'un processus métier.
5. **Paramétrage** = adapter l'ERP **sans modifier le code source**.
6. **Sur site** (contrôle) / **Cloud** (abonnement, Internet) / **hybride**.
7. **Odoo** = Python + PostgreSQL + vues XML.
8. Produits : **Goods 607/707**, **Expenses 606**, **Services 615**.
9. **Dispo = réel + en commande − réservé** ; si dispo < Min → **Max − dispo**.
10. **Trigger** = PL/SQL automatique sur INSERT/UPDATE/DELETE ; `:OLD` / `:NEW`.

![[ERP Revision Map.excalidraw|100%]]
