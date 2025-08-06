HC1T3 - Tâche 3 : Vérifier si un nombre est supérieur à 18
Voici une **présentation structurée** de ton exemple Haskell avec :


---

## ✅ 1. Définitions des concepts

### 🔹 Fonction pure

Une **fonction pure** dépend uniquement de ses entrées et produit toujours le même résultat sans effet de bord (pas d’affichage, de fichier, etc.).

Exemple :

```haskell
greaterThan18 20  -- retourne toujours True
```

---

### 🔹 Types `Int` et `Bool`

* `Int` : type entier (positif ou négatif)
* `Bool` : type booléen, dont les valeurs possibles sont **`True`** ou **`False`**

---

### 🔹 Opérateur `>`

L’opérateur `>` permet de vérifier si une valeur est **strictement supérieure** à une autre.
Par exemple : `x > 18` renvoie `True` si `x` est supérieur à 18.

---

## 💻 2. Code Haskell

```haskell
-- Fonction pure : vérifie si un nombre est supérieur à 18
greaterThan18 :: Int -> Bool
greaterThan18 x = x > 18

-- Programme principal sans saisie clavier
main :: IO ()
main = do
  -- Choix d'un nombre à tester (par exemple 20)
  let x = 20

  -- Appel de la fonction
  let result = greaterThan18 x

  -- Affichage du résultat
  putStrLn ("Est-ce que " ++ show x ++ " est supérieur à 18 ? " ++ show result)
```

---

## 📘 3. Explication 

### 🔸 Définition de la fonction `greaterThan18`

```haskell
greaterThan18 :: Int -> Bool
```

🔹 Déclare une fonction qui prend un entier (`Int`) et retourne un booléen (`Bool`).

```haskell
greaterThan18 x = x > 18
```

🔹 Compare `x` à 18.
Renvoie `True` si `x` est **strictement supérieur** à 18, sinon `False`.

---

### 🔸 Fonction principale `main`

```haskell
main :: IO ()
```

🔹 Indique que `main` est une fonction d’entrée/sortie (type `IO`) ne retournant rien (`()`).

```haskell
main = do
```

🔹 Démarre un bloc d'instructions IO.

```haskell
  let x = 20
```

🔹 Déclare une constante `x` avec la valeur `20`.

```haskell
  let result = greaterThan18 x
```

🔹 Applique la fonction `greaterThan18` à `x`, et stocke le résultat (`True` ou `False`) dans `result`.

```haskell
  putStrLn ("Est-ce que " ++ show x ++ " est supérieur à 18 ? " ++ show result)
```

🔹 Affiche le message final.
`show` convertit `x` et `result` (un entier et un booléen) en texte (`String`) pour pouvoir les concaténer.

---

