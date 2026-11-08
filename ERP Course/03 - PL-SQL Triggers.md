---
title: 03 - PL-SQL Triggers
tags:
  - erp
  - course
  - plsql
  - triggers
aliases:
  - PL/SQL et triggers
  - Déclencheurs
---

# 03 — PL/SQL et triggers

![[Database Trigger Flow.excalidraw|100%]]

## 1. Bloc PL/SQL

```sql
DECLARE
    -- déclarations (optionnel)
BEGIN
    -- instructions (obligatoire)
EXCEPTION
    -- erreurs (optionnel)
END;
```

- **SQL** = quoi faire (ensembliste) ; **PL/SQL** = comment le faire (procédural).
- Objets stockés en base : **procédures**, **fonctions**, **packages**, **triggers**.

## 2. Procédure vs fonction

| | Procédure | Fonction |
|---|---|---|
| Retour | Non (sauf paramètres `OUT`) | **Oui, `RETURN` obligatoire** |
| Appel | Explicite (`EXECUTE`) | Dans une expression / `SELECT` |

- **IN** : copie, non modifiable. **OUT** : NULL au départ, puis renvoyé. **IN OUT** : entrée, modifié, renvoyé.
- `%TYPE` = même type qu'une colonne (ex. `emp.ename%TYPE`).

## 3. Curseur (SELECT multi-lignes)

**4 étapes** : déclaration → `OPEN` → `FETCH … INTO` → `CLOSE`.
Fin de boucle : `EXIT WHEN curseur%NOTFOUND;`.

## 4. Exceptions

| Exception | Cause |
|---|---|
| `NO_DATA_FOUND` | Aucune ligne |
| `TOO_MANY_ROWS` | Plusieurs lignes |
| `VALUE_ERROR` | Erreur de conversion |
| `ZERO_DIVIDE` | Division par zéro |
| `OTHERS` | Toutes les autres |

- `DBMS_OUTPUT.PUT_LINE` = afficher ; `SQLERRM` = message d'erreur.

## 5. Trigger (déclencheur)

> [!important] Définition
> Bloc **PL/SQL stocké** qui s'exécute **automatiquement** sur un événement d'une **table**, une **vue** ou la **base**. On ne l'appelle jamais directement.

| Critère | Valeurs |
|---|---|
| Événement | `INSERT`, `UPDATE`, `DELETE` |
| Moment | `BEFORE`, `AFTER`, `INSTEAD OF` |
| Niveau | **table** (1 fois/instruction) ou **ligne** (`FOR EACH ROW`, 1 fois/ligne) |

- `:OLD` = valeurs **avant** ; `:NEW` = valeurs **après** (trigger ligne).
- Sert à : **règle métier**, **cohérence**, **audit**, **intégration des données**.

### Syntaxe

```sql
CREATE OR REPLACE TRIGGER nom_trigger
BEFORE | AFTER INSERT | UPDATE | DELETE
ON nom_table
[FOR EACH ROW]
[WHEN (condition)]
BEGIN
    -- :OLD.valeur / :NEW.valeur
END;
```

### Exemple — audit des salaires

```sql
CREATE OR REPLACE TRIGGER trg_audit_salaire
AFTER UPDATE OF sal ON emp
FOR EACH ROW
BEGIN
    INSERT INTO audit_salaire (empno, ancien_sal, nouveau_sal, date_modif)
    VALUES (:OLD.empno, :OLD.sal, :NEW.sal, SYSDATE);
END;
```

> [!warning] Limites
> Logique **cachée** (difficile à déboguer), risques de **cascades**, ralentit les écritures. Idéal pour l'**audit** et l'**intégrité** au niveau base.

## 6. Mini-test

> [!question]- Différence procédure / fonction ?
> La **fonction** retourne **obligatoirement** une valeur (`RETURN`).

> [!question]- Les 4 étapes d'un curseur ?
> Déclaration → `OPEN` → `FETCH` → `CLOSE`.

> [!question]- À quoi servent :OLD et :NEW ?
> `:OLD` = avant l'opération, `:NEW` = après (trigger ligne).

> [!question]- Trigger de table vs trigger de ligne ?
> Table = **1 fois par instruction** ; ligne (`FOR EACH ROW`) = **1 fois par ligne**.
