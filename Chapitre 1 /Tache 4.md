HC1T4 - Tâche 4 : Composer une fonction pour traiter des données de joueurs
import Data.List (sortBy)       -- Pour utiliser la fonction sortBy
import Data.Ord (comparing)     -- Pour comparer selon un critère

-- 1. Fonction pour extraire les noms de joueurs d'une liste de tuples (nom, score)
extractPlayers :: [(String, Int)] -> [String]
extractPlayers joueurs = [ nom | (nom, _) <- joueurs ]
-- Utilise une liste en compréhension pour récupérer le nom dans chaque tuple

-- 2. Fonction pour trier les joueurs selon leur score (ordre décroissant)
sortByScore :: [(String, Int)] -> [(String, Int)]
sortByScore joueurs = sortBy (flip (comparing snd)) joueurs
-- 'snd' récupère le score dans le tuple
-- 'comparing snd' trie par score croissant
-- 'flip' inverse pour avoir un tri décroissant

-- 3. Fonction pour récupérer les 3 premiers éléments d’une liste
topThree :: [a] -> [a]
topThree = take 3
-- 'take 3' prend les 3 premiers éléments d'une liste

-- 4. Fonction composée : trie, prend les 3 premiers, puis extrait les noms
getTopThreePlayers :: [(String, Int)] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore
-- On compose : d'abord trier, ensuite prendre les 3 premiers, enfin extraire les noms
main :: IO ()
main = do
  let joueurs = [("Alice", 12), ("Bob", 25), ("Charlie", 18), ("David", 30), ("Eve", 10)]
  let top = getTopThreePlayers joueurs
  putStrLn "Top 3 joueurs :"
  print top
