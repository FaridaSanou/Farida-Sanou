HC1T2 - Tâche 2 : Exemple de fonction pure

---

## ✅ 1. Définitions des concepts

### 🔹 Fonction pure

Une **fonction pure** en Haskell est une fonction qui :

* Donne toujours le **même résultat** pour les **mêmes arguments**
* **N’a aucun effet de bord** (pas de lecture/écriture de fichier, pas d’impression à l’écran, etc.)

> 💡 Exemple : `f x = x + 1` est pure. Elle ne dépend que de `x`.

---

### 🔹 Types numériques flottants (`Floating`)

Le type `Floating a` indique que `a` peut être un nombre à virgule flottante :

* `Float` (simple précision)
* ou `Double` (double précision)

Cela permet à la fonction de rester **générique** (flexible sur le type de nombre).

---

### 🔹 La constante `pi`

`pi` est une **constante prédéfinie** en Haskell représentant la valeur de π (\~ 3.14159), utilisable dans toute fonction de type `Floating`.

---

## 💻 2. Code Haskell

```haskell
-- Déclaration de la fonction circleArea
-- Elle prend un rayon (de type flottant) et retourne une aire (même type)
-- 'Floating a' signifie que 'a' peut être un Float ou un Double
circleArea :: Floating a => a -> a
circleArea r = pi * r^2  -- Aire d’un cercle : π * r²

-- Fonction principale (point d’entrée du programme)
main :: IO ()
main = do
  -- Déclaration d’un rayon fixe (ici 3.0)
  let rayon = 3.0

  -- Appel de la fonction circleArea avec ce rayon
  let aire = circleArea rayon

  -- Affichage du résultat à l'écran
  -- 'show' convertit les nombres en texte pour l’affichage
  putStrLn ("L'aire du cercle de rayon " ++ show rayon ++ " est " ++ show aire)
```

---

## 📘 3. Explications 

### 🔸 Fonction `circleArea`

```haskell
circleArea :: Floating a => a -> a
```

🔹 Ceci est l’**annotation de type** :

* La fonction prend un argument `r` de type `a` (où `a` est un type flottant)
* Elle retourne une valeur du même type `a`
  **`Floating a =>`** signifie que `a` doit être un type flottant (`Float` ou `Double`).

```haskell
circleArea r = pi * r^2
```

🔹 Définit la formule de l’aire d’un cercle :
**π × r²**, avec `^2` pour élever `r` au carré.

---

### 🔸 Fonction principale `main`

```haskell
main :: IO ()
```

🔹 Déclare que `main` est une action d’entrée/sortie (de type `IO`) qui ne retourne rien (`()`).

```haskell
main = do
```

🔹 Ouvre un bloc `do` pour enchaîner plusieurs actions IO.

```haskell
  let rayon = 3.0
```

🔹 Définit une constante `rayon` égale à 3.0 (un `Double` par défaut).

```haskell
  let aire = circleArea rayon
```

🔹 Appelle la fonction `circleArea` avec le rayon défini, et stocke le résultat dans `aire`.

```haskell
  putStrLn ("L'aire du cercle de rayon " ++ show rayon ++ " est " ++ show aire)
```

🔹 Affiche une phrase avec le rayon et l’aire calculée.
`show` transforme les valeurs numériques en texte (`String`) pour qu’elles soient concaténées dans l’affichage.

---



