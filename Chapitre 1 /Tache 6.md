HC1T6 - Tâche 6 : Utilisation de signatures de type
Voici la présentation complète de ton exemple sur l’**utilisation des signatures de type** en Haskell, avec :

---

## ✅ 1. Définitions des concepts

### 🔹 Signature de type (`::`)

Une **signature de type** permet d’indiquer **le type des paramètres et du résultat d’une fonction**.
Elle aide :

* à **mieux comprendre** la fonction
* à **éviter les erreurs**
* et à permettre au compilateur de vérifier la cohérence

Exemple :

```haskell
addNumbers :: Int -> Int -> Int
```

Cela signifie :

* La fonction prend **deux `Int`**
* Et retourne **un `Int`**

---

### 🔹 Types de base en Haskell

* `Int` : entier (positif ou négatif)
* `IO ()` : action d’entrée/sortie sans valeur de retour
* `String` : chaîne de caractères
* `Bool` : booléen (`True` ou `False`)

---

### 🔹 `show`

Fonction standard qui **convertit une valeur en chaîne de caractères**, pour pouvoir l’afficher avec `putStrLn`.

---

## 💻 2. Code Haskell

```haskell
-- Fonction qui additionne deux entiers
addNumbers :: Int -> Int -> Int
addNumbers x y = x + y

-- Fonction principale
main :: IO ()
main = do
  let a = 4
  let b = 7
  let somme = addNumbers a b
  putStrLn ("La somme de " ++ show a ++ " et " ++ show b ++ " est : " ++ show somme)
```

---

## 📘 3. Explication 

### 🔸 Fonction `addNumbers`

```haskell
addNumbers :: Int -> Int -> Int
```

🔹 **Signature de type** :

* Prend deux entiers `Int`
* Retourne un entier `Int`

```haskell
addNumbers x y = x + y
```

🔹 **Définition** : la somme des deux arguments `x` et `y`.

---

### 🔸 Fonction `main`

```haskell
main :: IO ()
```

🔹 Point d’entrée du programme, action d’entrée/sortie.

```haskell
main = do
  let a = 4
  let b = 7
```

🔹 Déclaration de deux entiers `a` et `b`.

```haskell
  let somme = addNumbers a b
```

🔹 Appel de la fonction `addNumbers` avec `a` et `b`, résultat stocké dans `somme`.

```haskell
  putStrLn ("La somme de " ++ show a ++ " et " ++ show b ++ " est : " ++ show somme)
```

🔹 Affiche une phrase contenant `a`, `b`, et leur somme.
`show` convertit les valeurs numériques en chaînes de caractères.

---




