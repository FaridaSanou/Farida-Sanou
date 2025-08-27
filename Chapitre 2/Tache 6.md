HC2T6 - Tâche 6 : Comprendre Int vs Luge

---

## 1️⃣ Déclaration des variables

En Haskell, on peut déclarer les variables immuables ainsi :

```haskell
-- un Int (entier borné, généralement sur 64 bits)
variableNombre :: Int
variableNombre = 2 ^ 62   -- 2 puissance 62

-- un Integer (entier arbitrairement grand, sans limite de taille)
bigNumber :: Integer
bigNumber = 2 ^ 127       -- 2 puissance 127
```

---

## 2️⃣ Différence entre `Int` et `Integer`

* **`Int`** : entier **borné** (taille limitée, dépend de l’architecture, souvent 64 bits). Peut provoquer un **dépassement** (overflow).
* **`Integer`** : entier **non borné** (arbitrairement grand). Pas de dépassement, mais un peu plus lent.

---

## 3️⃣ Évaluer `2^64 :: Int` dans GHCi

Si on ouvre GHCi et tapes :

```haskell
Prelude> 2^64 :: Int
```

on n’obtient **pas 18 446 744 073 709 551 616** (qui est la vraie valeur de 2^64), mais plutôt :

```
0
```

 Pourquoi ? Parce que `Int` est limité à **64 bits signés**.

* La plus grande valeur possible est `2^63 - 1 = 9 223 372 036 854 775 807`.
* Comme `2^64` dépasse cette limite, le résultat **déborde** et revient à `0` (comportement de l’overflow).

---

## 4️⃣ Test avec `Integer`

Si on utilise `Integer`, pas de problème :

```haskell
Prelude> 2^64 :: Integer
18446744073709551616
```

---

 **Résumé :**

* `variableNombre = 2^62 :: Int` fonctionne, car c’est encore dans la limite du `Int`.
* `bigNumber = 2^127 :: Integer` fonctionne aussi, car `Integer` n’a pas de limite.
* `2^64 :: Int` provoque un **overflow** et retourne `0` au lieu du vrai résultat.

