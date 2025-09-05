HC3T2 - Tâche 2 : Déterminer la note à partir d'un score avec des gardes

---

##  Définition de la fonction avec gardes

```haskell
-- Signature
grade :: Int -> String

-- Définition avec gardes
grade score
    | score >= 90 = "A"
    | score >= 80 = "B"
    | score >= 70 = "C"
    | score >= 60 = "D"
    | otherwise   = "F"
```

---

##  Explication

* Les gardes `|` permettent de tester plusieurs conditions dans l’ordre.
* La première condition vraie est utilisée.
* `otherwise` est équivalent à `True`, donc c’est le cas par défaut (ici quand la note est < 60).

---

##  Exemple de test (dans `main`)

```haskell
main :: IO ()
main = do
    print (grade 95)  -- "A"
    print (grade 72)  -- "C"
    print (grade 50)  -- "F"
```

