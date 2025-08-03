HC1T5 - Tâche 5 : Paresse en Haskell
-- 1. Définir une fonction qui génère une liste infinie de nombres entiers croissants
infiniteNumbers :: [Int]
infiniteNumbers = [1..]
-- [1..] signifie "la liste des entiers à partir de 1 jusqu'à l'infini"

-- 2. Fonction pour extraire les n premiers nombres de cette liste infinie
firstN :: Int -> [Int]
firstN n = take n infiniteNumbers
-- 'take n' prend les n premiers éléments d'une liste (même infinie, grâce à la paresse)
main :: IO ()
main = do
  let n = 10  -- On veut les 10 premiers nombres
  let liste = firstN n
  putStrLn ("Les " ++ show n ++ " premiers nombres sont :")
  print liste
