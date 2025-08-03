HC1T6 - Tâche 6 : Utilisation de signatures de type
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
