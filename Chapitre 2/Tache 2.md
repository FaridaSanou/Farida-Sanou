HC2T2 - Tâche 2 : Signatures de fonctions

Une signature de fonction est une déclaration du type d’une fonction. Elle précise :
Le type des arguments que la fonction accepte.
Le type du résultat que la fonction retourne.
---

## 1️⃣ Fonction `ajouter`

### Signature

* Elle prend deux `Int` et retourne leur somme (`Int`) :

```haskell
ajouter :: Int -> Int -> Int
```

### Implémentation

```haskell
ajouter x y = x + y
```

---

## 2️⃣ Fonction `isEven`

* Elle prend un `Int` et retourne un `Bool` (`True` si le nombre est pair, `False` sinon) :

### Signature

```haskell
isEven :: Int -> Bool
```

### Implémentation

```haskell
isEven n = n `mod` 2 == 0
```

Ici, `mod` calcule le reste de la division entière.

---

## 3️⃣ Fonction `concatStrings`

* Elle prend deux `String` et retourne leur concaténation :

### Signature

```haskell
concatStrings :: String -> String -> String
```

### Implémentation

```haskell
concatStrings s1 s2 = s1 ++ s2
```

 `++` est l’opérateur de concaténation de listes (les `String` sont des listes de `Char` en Haskell).

---

## ✅ Exemple d’utilisation dans GHCi

```haskell
Prelude> ajouter 5 7
12

Prelude> isEven 4
True

Prelude> isEven 9
False

Prelude> concatStrings "Hello " "World"
"Hello World"
```

---


