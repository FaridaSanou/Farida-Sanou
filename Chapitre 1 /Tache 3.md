HC1T3 - Tâche 3 : Vérifier si un nombre est supérieur à 18
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
