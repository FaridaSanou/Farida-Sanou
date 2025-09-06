HC3T4 - Tâche 4 : Calculer l’aire d’un triangle avec la formule de Héron

---

---

##  Définition de la fonction

```haskell
-- Signature
triangleArea :: Float -> Float -> Float -> Float

-- Définition avec let
triangleArea a b c =
    let s = (a + b + c) / 2   -- demi-périmètre
    in sqrt (s * (s - a) * (s - b) * (s - c))
```

---

##  Explication

* La formule de Héron :

  $$
  \text{Aire} = \sqrt{s (s - a)(s - b)(s - c)}
  $$

  où $s = \frac{a+b+c}{2}$ est le demi-périmètre.
* On utilise `let` pour définir `s`.
* `sqrt` est la racine carrée.

---

##  Exemple de test (dans `main`)

```haskell
main :: IO ()
main = do
    print (triangleArea 3 4 5)   -- triangle rectangle (aire attendue = 6)
    print (triangleArea 7 8 9)   -- aire ≈ 26.83
```

---


👉 Veux-tu que je te montre aussi une **version avec des gardes (`|`)** qui vérifie si les côtés donnés peuvent former un triangle (condition de validité) avant de calculer l’aire ?
