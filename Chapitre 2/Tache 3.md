HC2T3 - Tâche 3 : Variables d'économie


En Haskell, **toutes les variables sont immuables**, c’est-à-dire qu’une fois assignée, leur valeur **ne peut pas changer**.

---

## 1️⃣ Déclaration de variables immuables

```haskell
-- Déclarations
myAge :: Int
myAge = 21

piValue :: Double
piValue = 3.14159

salutation :: String
salutation = "Bonjour Haskell !"

isHaskellFun :: Bool
isHaskellFun = True
```

> Remarques :

* Les types sont **facultatifs** mais fortement recommandés.
* Les noms commencent par une **lettre minuscule** par convention.

---

## 2️⃣ Tester l’immuabilité

Essayons de **modifier une variable**, par exemple :

```haskell
myAge = 25
```

Haskell donne une **erreur** dans GHCi ou lors de la compilation :

```
<interactive>: ...: error: Multiple declarations of ‘myAge’
```

> Explication :
> En Haskell, on **ne peut pas réassigner** une valeur à une variable déjà définie. Si on veut une “nouvelle valeur”, il faut **déclarer une nouvelle variable** :

```haskell
myNewAge :: Int
myNewAge = 25
```

---
