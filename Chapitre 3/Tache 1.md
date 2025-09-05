HC3T1 - Tâche 1 : Vérifiant si un nombre de nombres positifs, négatif ou nul

une fonction Haskell qui teste si un nombre est positif, négatif ou nul, en utilisant `if-then-else`.

---

##  Définition de la fonction

```haskell
-- Signature
checkNumber :: Int -> String

-- Définition avec if-then-else
checkNumber n =
    if n > 0 then "Positif"
    else if n < 0 then "Négatif"
    else "Zéro"
```

---

##  Explication

* `checkNumber` prend un entier (`Int`).
* Si `n > 0`, elle retourne `"Positif"`.
* Sinon, si `n < 0`, elle retourne `"Négatif"`.
* Sinon (donc `n == 0`), elle retourne `"Zéro"`.

---

##  Exemple d’utilisation (dans `main`)

```haskell
main :: IO ()
main = do
    print (checkNumber 5)     -- "Positif"
    print (checkNumber (-3))  -- "Négatif"
    print (checkNumber 0)     -- "Zéro"
```

