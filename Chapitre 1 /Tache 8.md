HC1T8 - Tâche 8 : Fonctions d’ordre supérieur

---

## ✅ 1. Définitions des concepts

### 🔹 Fonction d’ordre supérieur

Une **fonction d’ordre supérieur** est une fonction qui :

* **prend une ou plusieurs fonctions** comme argument(s),
* **et/ou retourne une fonction** en résultat.

En Haskell, les fonctions sont des valeurs de première classe : on peut les manipuler comme des nombres ou des chaînes.

---

### 🔹 Exemple : `applyTwice`

La fonction `applyTwice` applique **deux fois** une fonction à une valeur.

**Exemple :**

```haskell
applyTwice (+3) 4
```

* `+3` est une fonction : elle ajoute 3
* `applyTwice` va faire : `+3 (+3 4)` → `+3 (7)` → `10`

---

### 🔹 Signature de type

```haskell
applyTwice :: (a -> a) -> a -> a
```

* `(a -> a)` : une fonction qui prend un type `a` et retourne un type `a`
* `a` : une valeur de ce type
* `-> a` : le résultat final

Cette signature est **générique** : `a` peut être un `Int`, `Float`, `String`, etc.

---

## 💻 2. Code Haskell

```haskell
-- Fonction d’ordre supérieur : applique une fonction deux fois
applyTwice :: (a -> a) -> a -> a
applyTwice f x = f (f x)

-- Exemple d’utilisation dans main
main :: IO ()
main = do
  let result = applyTwice (+3) 4  -- (4 + 3 = 7, puis 7 + 3 = 10)
  putStrLn ("Résultat : " ++ show result)
```

---

## 📘 3. Explication 

### 🔸 Fonction `applyTwice`

```haskell
applyTwice :: (a -> a) -> a -> a
```

🔹 Signature de type :

* Prend une **fonction** `f` : `(a -> a)`
* Prend une **valeur** `x` : `a`
* Retourne une **valeur** de type `a`

```haskell
applyTwice f x = f (f x)
```

🔹 Applique deux fois la fonction `f` à `x` :

* `f x` calcule un premier résultat
* Puis on applique `f` une seconde fois sur ce résultat

---

### 🔸 Fonction `main`

```haskell
main :: IO ()
```

🔹 Début du programme principal

```haskell
let result = applyTwice (+3) 4
```

🔹 Applique `+3` deux fois à 4 :

* `+3 4 = 7`
* `+3 7 = 10`
* Donc `result = 10`

```haskell
putStrLn ("Résultat : " ++ show result)
```

🔹 Affiche : `Résultat : 10`

---


