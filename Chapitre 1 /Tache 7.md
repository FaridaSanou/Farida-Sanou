HC1T7 - Tâche 7 : Conversion Fahrenheit/Celsius
---

## ✅ 1. Définitions des concepts

### 🔹 Conversion de température

Pour convertir une température de **Fahrenheit vers Celsius**, on utilise la formule :

```
C = (5 / 9) * (F - 32)
```

Où :

* `F` est la température en Fahrenheit
* `C` est la température en Celsius

---

### 🔹 Types numériques génériques (`Floating a => a`)

```haskell
fToC :: Floating a => a -> a
```

Cela signifie :

* La fonction prend un nombre `f` de **type flottant** (`Float`, `Double`, etc.)
* Et retourne un nombre du même type

Le mot-clé **`Floating a =>`** précise que `a` doit appartenir à la classe des **types flottants** (nombres à virgule).

---

### 🔹 `show` pour l'affichage

`show` est une fonction qui convertit une **valeur numérique en chaîne de caractères**, nécessaire pour l’afficher avec `putStrLn`.

---

## 💻 2. Code Haskell

```haskell
-- Fonction de conversion Fahrenheit → Celsius
fToC :: Floating a => a -> a
fToC f = (5 / 9) * (f - 32)

-- Fonction principale
main :: IO ()
main = do
  let fahrenheit = 98.6
  let celsius = fToC fahrenheit
  putStrLn ("La température " ++ show fahrenheit ++ "°F équivaut à " ++ show celsius ++ "°C")
```

---

## 📘 3. Explication 

### 🔸 Fonction `fToC`

```haskell
fToC :: Floating a => a -> a
```

🔹 Déclare que `fToC` est une fonction prenant un nombre flottant et en retournant un autre.
Elle peut fonctionner avec des `Float`, `Double`, etc.

```haskell
fToC f = (5 / 9) * (f - 32)
```

🔹 Applique la formule mathématique de conversion :

* On soustrait 32 à la température en Fahrenheit
* Puis on multiplie par 5/9 pour obtenir les Celsius

---

### 🔸 Fonction `main`

```haskell
main :: IO ()
```

🔹 Point d’entrée du programme (action d’entrée/sortie, ne retourne rien).

```haskell
main = do
  let fahrenheit = 98.6
```

🔹 Déclare une température `fahrenheit` à convertir (98.6°F, température du corps humain).

```haskell
  let celsius = fToC fahrenheit
```

🔹 Calcule l'équivalent en Celsius grâce à la fonction `fToC`.

```haskell
  putStrLn ("La température " ++ show fahrenheit ++ "°F équivaut à " ++ show celsius ++ "°C")
```

🔹 Affiche le résultat de la conversion avec `show` pour convertir les nombres en texte.

---


