---
title: 05 - Cheat Sheet
tags:
  - erp
  - course
  - cheatsheet
aliases:
  - Fiche révision ERP
---

# 05 — Fiche de révision

## Définitions

| Terme | Définition |
|---|---|
| **SI** | Collecter, stocker, traiter, diffuser l'information pour décider |
| **Processus** | Enchaînement **transversal** d'activités à valeur ajoutée (« quoi faire ») |
| **Procédure** | Manière de mettre en œuvre (« comment faire ») |
| **Workflow** | **Automatisation** d'un processus métier |
| **ERP / PGI** | Modules interconnectés + **base unique et partagée**, centralise et automatise |
| **Paramétrage** | Adapter **sans modifier le code source** |
| **Traçabilité** | Retrouver l'origine d'une information → audit |

## Avec vs sans ERP

| Sans ERP | Avec ERP |
|---|---|
| Vertical (silos) | Transversal |
| Bases multiples | Base unique |
| Redondance | Saisie unique |
| Vision partielle | Vision globale, temps réel |

**Avantages** : cohérence, vision globale, automatisation, traçabilité, reporting.
**Risques** : dépendance éditeur, sécurité, panne totale, surcoût, résistance au changement.

## Déploiement

| Mode | Points clés |
|---|---|
| **Sur site** | Contrôle + sécurité + personnalisation ; coût, maintenance, MAJ complexes |
| **Web sur site** | Sur site + accès navigateur ; failles web |
| **Cloud** | Abonnement, Internet, MAJ auto, scalable ; dépendance Internet |
| **Hybride** | Site + cloud |

Généraliste (SAP, Oracle) / spécialisé (Infor, CliniSys) — propriétaire (SAP, NetSuite) / open source (Odoo, Open-Prod).
Historique : 1990 Gartner → 1992 SAP R/3 → 2000 Web → 2010 Cloud → 2020 Hybride.

## Odoo

| Élément | Valeur |
|---|---|
| Nature | ERP modulaire, open source |
| Création | **2002**, Fabien Pinckaers |
| Versions | Community (gratuit) / Enterprise (payant) |
| Langage / SGBD / vues | **Python / PostgreSQL / XML** |
| Module / init / droits | `__manifest__.py` / `__init__.py` / `security/ir.model.access.csv` |
| Domain | **Filtre** |
| Personnaliser | **Étendre** (ne pas modifier la source) |
| Mode dev | `?debug=1` / `?debug=0` / `?debug=assets` |
| Repère | Scarabée · Ctrl + K |

**Base edu** : préfixe `edu-` (2 ans), connexion tous les 3 mois, `edu-Matricule-Groupe`, pays Tunisie, activation sous 3 h.

## Achats et réappro

**Flux** : Demande de prix → Bon de commande → Réception → Facture.

| Catégorie | Stocké | Compte |
|---|---|---|
| Goods | Oui | **607 / 707** |
| Expenses | Non | **606** |
| Services | Non | **615** |

> [!important] Formules
> **Dispo = réel + en commande − réservé**
>
> Si **dispo < Min** → **à commander = Max − dispo**

Exemple : Max 20, dispo −18 → **38**.

## PL/SQL

| Objet | Retour | Appel |
|---|---|---|
| Procédure | Non (sauf `OUT`) | Explicite |
| Fonction | **Oui** (`RETURN`) | Dans une expression |
| Curseur | Lignes | OPEN / FETCH / CLOSE |
| Trigger | Non | **Automatique** |

- **IN** : copie non modifiable · **OUT** : NULL puis renvoyé · **IN OUT** : entrée + sortie.
- Exceptions : `NO_DATA_FOUND`, `TOO_MANY_ROWS`, `VALUE_ERROR`, `ZERO_DIVIDE`, `OTHERS`.

### Trigger

```sql
CREATE OR REPLACE TRIGGER nom_trigger
BEFORE | AFTER INSERT | UPDATE | DELETE
ON table
FOR EACH ROW
BEGIN
    -- :OLD.valeur / :NEW.valeur
END;
```

- Table = 1 fois/instruction ; ligne (`FOR EACH ROW`) = 1 fois/ligne.
- `:OLD` = avant, `:NEW` = après.

## Les 10 pièges

1. Processus ≠ procédure.
2. Workflow = automatisation, pas un processus d'achat.
3. Horizontal = tous secteurs ; vertical = un secteur.
4. Cloud = abonnement + accès distant.
5. ERP = **base unique**, pas multiple.
6. Odoo = Python + PostgreSQL + XML.
7. Droits = `security/ir.model.access.csv`.
8. Vue Odoo = interface (≠ vue SQL).
9. Personnaliser = étendre.
10. Réappro = **dispo** (pas le seul stock réel).
