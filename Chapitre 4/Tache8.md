HC4T8 - Tâche 8 : Extraire des valeurs de tuples
```haskell
-- HC4T8 - Tâche 8 : Extraire des valeurs de tuples
-- On définit une fonction describeTuple qui prend un tuple (a, b)
-- et renvoie une phrase décrivant les deux valeurs.

describeTuple :: (Show a, Show b) => (a, b) -> String
describeTuple (x, y) =
    "Le tuple contient la première valeur : " ++ show x ++
    " et la deuxième valeur : " ++ show y
```

---

 **Explications :**

* `(x, y)` → c’est le **pattern matching** qui permet d’extraire les deux éléments du tuple.
* `show` → convertit une valeur en texte pour pouvoir l’afficher.
* `++` → sert à **concaténer** (coller) des chaînes de caractères.
* `(Show a, Show b)` → indique que les deux types doivent pouvoir être affichés (sinon `show` ne fonctionnerait pas).

---
 **Exemples de tests :**

```haskell
main :: IO ()
main = do
    putStrLn (describeTuple (10, "Bonjour"))
    putStrLn (describeTuple ("Rouge", 42))
    putStrLn (describeTuple (3.14, True))
```


