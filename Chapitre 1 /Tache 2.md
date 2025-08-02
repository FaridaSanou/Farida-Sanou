HC1T2 - Tâche 2 : Exemple de fonction pure
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
