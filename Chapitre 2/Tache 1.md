HC2T1 - Tâche 1 : Vérification des types dans GHCi
---

## 1. Expression : `42`

Un entier comme `42` est par défaut un **nombre entier polymorphe** en Haskell.
En effet, Haskell ne le considère pas seulement comme `Int`, mais comme tout type qui appartient à la classe de type `Num`.

👉 **Type attendu** :

```haskell
42 :: Num a => a
```

Cela signifie : "`42` peut être utilisé comme n’importe quel type numérique (`Int`, `Integer`, `Double`, …)".

👉 **Dans GHCi** :

```haskell
Prelude> :t 42
42 :: Num a => a
```

---

## 2. Expression : `3.14`

Un nombre à virgule est un **littéral flottant**. Par défaut, Haskell le met dans la classe `Fractional`, qui regroupe les nombres décimaux (`Float`, `Double`, …).

👉 **Type attendu** :

```haskell
3.14 :: Fractional a => a
```

👉 **Dans GHCi** :

```haskell
Prelude> :t 3.14
3.14 :: Fractional a => a
```

---

## 3. Expression : `"Haskell"`

Une chaîne de caractères en Haskell est en réalité une **liste de caractères**, donc de type `[Char]`.

👉 **Type attendu** :

```haskell
"Haskell" :: [Char]
```

👉 **Dans GHCi** :

```haskell
Prelude> :t "Haskell"
"Haskell" :: [Char]
```

---

## 4. Expression : `'Z'`

Une seule lettre entre `' '` est un caractère unique, donc de type `Char`.

👉 **Type attendu** :

```haskell
'Z' :: Char
```

👉 **Dans GHCi** :

```haskell
Prelude> :t 'Z'
'Z' :: Char
```

---

## 5. Expression : `True && False`

* `True` et `False` sont des valeurs booléennes (`Bool`).
* L’opérateur `(&&)` a pour type `Bool -> Bool -> Bool`.
  Donc l’expression `True && False` est une **valeur de type Bool**.

👉 **Type attendu** :

```haskell
True && False :: Bool
```

👉 **Dans GHCi** :

```haskell
Prelude> :t True && False
True && False :: Bool
```

---

✅ **Résumé des types:

| Expression      | Type trouvé         |
| --------------- | ------------------- |
| `42`            | `Num a => a`        |
| `3.14`          | `Fractional a => a` |
| `"Haskell"`     | `[Char]`            |
| `'Z'`           | `Char`              |
| `True && False` | `Bool`              |

---


