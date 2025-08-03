HC1T8 - Tâche 8 : Fonctions d’ordre supérieur
-- Fonction d’ordre supérieur : applique une fonction deux fois
applyTwice :: (a -> a) -> a -> a
applyTwice f x = f (f x)

-- Exemple d’utilisation dans main
main :: IO ()
main = do
  let result = applyTwice (+3) 4  -- (4 + 3 = 7, puis 7 + 3 = 10)
  putStrLn ("Résultat : " ++ show result)
{- Explication ligne par ligne :
🔸 applyTwice :: (a -> a) -> a -> a
C’est la signature de type :

(a -> a) : la fonction f prend un a et retourne un a.

a : la valeur à laquelle on applique f.

-> a : le résultat final (même type a).

Cela veut dire que applyTwice est générique : elle peut fonctionner avec n’importe quel type a, tant que f est une fonction a -> a -}
