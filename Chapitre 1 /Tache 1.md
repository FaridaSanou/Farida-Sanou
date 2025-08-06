HC1T1 - Tâche 1 : Composition de fonctions

---

## ✅ 1. Définitions des concepts

### 🔹 Fonction

En Haskell, une **fonction** prend un ou plusieurs arguments et retourne un résultat. Elle est définie par :

```haskell
nomFonction :: TypeEntrée -> TypeSortie
nomFonction argument = expression
```

### 🔹 Composition de fonctions

La **composition de fonctions** permet de combiner deux fonctions en une seule.
En Haskell, on utilise l'opérateur `(.)` :

```haskell
(f . g) x = f (g x)
```

Cela signifie : **appliquer `g` d'abord, puis appliquer `f` au résultat**.

### 🔹 Entrée/Sortie (`IO`)

Le type `IO` est utilisé pour les opérations d’entrée/sortie (affichage, lecture, etc.). Une fonction comme `main :: IO ()` permet d’exécuter un programme.

---

## 💻 2. Code Haskell

```haskell
-- Définition des fonctions
double :: Int -> Int
double x = x * 2

increment :: Int -> Int
increment x = x + 1

-- Composition : appliquer double puis increment
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Programme principal pour tester
main :: IO ()
main = do
  let x = 3
  let result = doubleThenIncrement x
  putStrLn ("Résultat : " ++ show result)
```

---

## 📘 3. Explication 

### 🔸 Définition des fonctions simples

```haskell
double :: Int -> Int
```

Déclare que `double` est une fonction qui prend un entier (`Int`) et retourne un entier.

```haskell
double x = x * 2
```

La fonction `double` retourne le double de `x`.

```haskell
increment :: Int -> Int
```

La fonction `increment` prend aussi un `Int` et retourne un `Int`.

```haskell
increment x = x + 1
```

Elle ajoute 1 à `x`.

---

### 🔸 Composition de fonctions

```haskell
doubleThenIncrement :: Int -> Int
```

Déclare une fonction composée : prend un entier et retourne un entier.

```haskell
doubleThenIncrement = increment . double
```

Utilise la **composition** :

* `double` est appliqué d'abord
* puis `increment` est appliqué au résultat
  Exemple :

```haskell
doubleThenIncrement 3 = increment (double 3) = increment 6 = 7
```

---

### 🔸 Partie principale du programme

```haskell
main :: IO ()
```

C’est la fonction principale, de type **IO** (entrée/sortie), ne retournant rien (`()`).

```haskell
main = do
```

Démarre un bloc d’instructions **IO**.

```haskell
  let x = 3
```

Déclare une constante `x` égale à 3.

```haskell
  let result = doubleThenIncrement x
```

Applique `doubleThenIncrement` à `x` et stocke le résultat.

```haskell
  putStrLn ("Résultat : " ++ show result)
```

Affiche le texte `"Résultat : "` suivi de la **valeur numérique** convertie en chaîne avec `show`.

---


