HC1T4 - Tâche 4 : Composer une fonction pour traiter des données de joueurs

---

## ✅ 1. Définitions des concepts

### 🔹 Tuple `(String, Int)`

Chaque joueur est représenté comme un **couple** (ou *tuple*) contenant :

* Un **nom** (`String`)
* Un **score** (`Int`)

Exemple : `("Alice", 12)` signifie que **Alice a un score de 12**.

---

### 🔹 Fonction `sortBy` et `comparing`

* `sortBy` trie une liste selon un critère défini
* `comparing snd` trie en fonction du **deuxième élément du tuple** (le score)
* `flip` inverse l’ordre, donc on obtient un **tri décroissant** (du plus grand au plus petit score)

---

### 🔹 Composition de fonctions

La fonction `getTopThreePlayers` est une **fonction composée** :

```haskell
getTopThreePlayers = extractPlayers . topThree . sortByScore
```

Elle combine **trois fonctions** :

1. `sortByScore` trie les joueurs
2. `topThree` prend les 3 premiers
3. `extractPlayers` garde uniquement les noms

---

## 💻 2. Code Haskell

```haskell
import Data.List (sortBy)       -- Pour trier une liste selon un critère
import Data.Ord (comparing)     -- Pour faciliter la comparaison

-- 1. Extraire les noms des joueurs à partir d'une liste (nom, score)
extractPlayers :: [(String, Int)] -> [String]
extractPlayers joueurs = [ nom | (nom, _) <- joueurs ]

-- 2. Trier les joueurs par score décroissant
sortByScore :: [(String, Int)] -> [(String, Int)]
sortByScore joueurs = sortBy (flip (comparing snd)) joueurs

-- 3. Prendre les 3 premiers éléments d’une liste
topThree :: [a] -> [a]
topThree = take 3

-- 4. Composer les trois fonctions pour obtenir les 3 meilleurs joueurs
getTopThreePlayers :: [(String, Int)] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore

-- Programme principal
main :: IO ()
main = do
  -- Liste des joueurs avec leurs scores
  let joueurs = [("Alice", 12), ("Bob", 25), ("Charlie", 18), ("David", 30), ("Eve", 10)]
  
  -- Appel de la fonction composée pour obtenir le top 3
  let top = getTopThreePlayers joueurs
  
  -- Affichage du résultat
  putStrLn "Top 3 joueurs :"
  print top
```

---

## 📘 3. Explication 

### 🔸 Imports

```haskell
import Data.List (sortBy)
import Data.Ord (comparing)
```

🔹 On importe les fonctions nécessaires pour trier selon des critères personnalisés.

---

### 🔸 Fonction `extractPlayers`

```haskell
extractPlayers :: [(String, Int)] -> [String]
extractPlayers joueurs = [ nom | (nom, _) <- joueurs ]
```

🔹 Utilise une **compréhension de liste** pour extraire les noms à partir des tuples.

---

### 🔸 Fonction `sortByScore`

```haskell
sortByScore :: [(String, Int)] -> [(String, Int)]
sortByScore joueurs = sortBy (flip (comparing snd)) joueurs
```

🔹 Trie la liste par score **du plus élevé au plus faible**.

---

### 🔸 Fonction `topThree`

```haskell
topThree :: [a] -> [a]
topThree = take 3
```

🔹 Garde les **3 premiers** éléments de la liste.

---

### 🔸 Fonction composée `getTopThreePlayers`

```haskell
getTopThreePlayers = extractPlayers . topThree . sortByScore
```

🔹 Combine les trois fonctions pour :

1. Trier la liste
2. Prendre les 3 premiers
3. Extraire les noms

---

### 🔸 Fonction `main`

```haskell
main = do
  let joueurs = [("Alice", 12), ("Bob", 25), ("Charlie", 18), ("David", 30), ("Eve", 10)]
  let top = getTopThreePlayers joueurs
  putStrLn "Top 3 joueurs :"
  print top
```

🔹 Crée une liste de joueurs, applique la fonction composée, et affiche le résultat.

---


