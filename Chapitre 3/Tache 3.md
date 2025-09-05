HC3T3 - Tâche 3 : Convertir une couleur RGB en chaîne hexadécimale avec let

 écrivons une fonction Haskell qui prend un triplet (R, G, B) et le convertit en une chaîne hexadécimale (par ex. `#FF007F`). On va utiliser `let` pour formater les valeurs.

---

##  Définition de la fonction

```haskell
import Text.Printf (printf)

-- Signature
rgbToHex :: (Int, Int, Int) -> String

-- Définition
rgbToHex (r, g, b) =
    let rh = printf "%02X" r  -- formater R en deux caractères hexadécimaux
        gh = printf "%02X" g  -- idem pour G
        bh = printf "%02X" b  -- idem pour B
    in "#" ++ rh ++ gh ++ bh   -- concaténation
```

---

##  Explication

* On utilise `let` pour définir des variables locales (`rh`, `gh`, `bh`).
* La fonction `printf "%02X"` formate un entier en **hexadécimal sur 2 caractères** (par ex. `0` devient `"00"`, `127` devient `"7F"`).
* Enfin, on concatène le tout avec `#` au début pour obtenir la couleur hexadécimale standard.

---

##  Exemple de test (dans `main`)

```haskell
main :: IO ()
main = do
    print (rgbToHex (255, 0, 127))   -- "#FF007F"
    print (rgbToHex (0, 255, 64))    -- "#00FF40"
```




👉 Veux-tu que je t’explique aussi **comment écrire cette fonction sans `printf`**, en utilisant la fonction standard `Numeric.showHex` ?
