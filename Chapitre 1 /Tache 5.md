HC1T5 - Tâche 5 : Paresse en Haskell

---

## ✅ 1. Définitions des concepts

### 🔹 Paresse (Laziness) en Haskell

La **paresse**, ou **évaluation paresseuse** (*lazy evaluation*), signifie que **Haskell ne calcule une expression que lorsqu’elle est nécessaire**.

> 💡 Exemple :
> Même si on crée une **liste infinie**, on peut en extraire les 10 premiers éléments **sans évaluer le reste**.

Cela permet :

* De manipuler des **structures infinies**
* De **gagner en efficacité** (on ne calcule que ce qu'on utilise)

---

### 🔹 Liste infinie

En Haskell, `[1..]` signifie :

> Une liste d’entiers **qui commence à 1 et continue sans fin**

Grâce à la **paresse**, cette liste est **générée au fur et à mesure**, et **jamais entièrement en mémoire**.

---

## 💻 2. Code Haskell

```haskell
-- 1. Définir une fonction qui génère une liste infinie de nombres entiers croissants
infiniteNumbers :: [Int]
infiniteNumbers = [1..]
-- [1..] signifie "la liste des entiers à partir de 1 jusqu'à l'infini"

-- 2. Fonction pour extraire les n premiers nombres de cette liste infinie
firstN :: Int -> [Int]
firstN n = take n infiniteNumbers
-- 'take n' prend les n premiers éléments d'une liste (même infinie, grâce à la paresse)

-- Programme principal
main :: IO ()
main = do
  let n = 10  -- On veut les 10 premiers nombres
  let liste = firstN n
  putStrLn ("Les " ++ show n ++ " premiers nombres sont :")
  print liste
```

---

## 📘 3. Explication 

### 🔸 Fonction `infiniteNumbers`

```haskell
infiniteNumbers :: [Int]
```

🔹 Déclare que la variable `infiniteNumbers` est une **liste d'entiers**.

```haskell
infiniteNumbers = [1..]
```

🔹 Définit une **liste infinie** à partir de `1`.
Grâce à la **paresse**, cette liste est **calculée à la demande**.

---

### 🔸 Fonction `firstN`

```haskell
firstN :: Int -> [Int]
```

🔹 `firstN` prend un entier (le nombre d’éléments à extraire) et retourne une liste d'entiers.

```haskell
firstN n = take n infiniteNumbers
```

🔹 `take n` extrait **les `n` premiers éléments** de la liste infinie.
Même si la liste est infinie, cela fonctionne sans erreur **grâce à la paresse**.

---

### 🔸 Fonction `main`

```haskell
main :: IO ()
```

🔹 Point d’entrée du programme, de type `IO ()`.

```haskell
main = do
  let n = 10
```

🔹 Déclare que l’on souhaite obtenir les 10 premiers nombres.

```haskell
  let liste = firstN n
```

🔹 Appelle `firstN` pour extraire les 10 premiers entiers.

```haskell
  putStrLn ("Les " ++ show n ++ " premiers nombres sont :")
```

🔹 Affiche un message explicatif.
`show` convertit le nombre `n` en texte.

```haskell
  print liste
```

🔹 Affiche la liste résultante `[1,2,3,4,5,6,7,8,9,10]`.

---



