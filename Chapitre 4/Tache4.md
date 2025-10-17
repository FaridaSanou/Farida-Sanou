HC4T4 - Tâche 4 : Réécrire specialBirthday avec le pattern matching

```haskell
-- Définition de la fonction specialBirthday
-- Cette fonction prend un âge (Int)
-- et renvoie un message spécial selon la valeur de l’âge.

specialBirthday :: Int -> String
-- Cas 1 : si la personne a 1 an
specialBirthday 1 = "Joyeux 1er anniversaire !"
-- Cas 2 : si la personne a 18 ans
specialBirthday 18 = "Félicitations pour ta majorité !"
-- Cas 3 : si la personne a 50 ans
specialBirthday 50 = "Bon demi-siècle !"
-- Cas 4 : si la personne a 100 ans
specialBirthday 100 = "Un siècle de vie, incroyable !"
-- Cas par défaut : pour tout autre âge
specialBirthday _ = "Joyeux anniversaire !"
```

---

 **Explications**

1. **`specialBirthday :: Int -> String`**
   → La signature indique que la fonction prend un **entier (`Int`)** et renvoie une **chaîne (`String`)**.

2. **Pattern matching sur la valeur :**

   * Si la valeur est exactement `1` → `"Joyeux 1er anniversaire !"`
   * Si la valeur est `18` → `"Félicitations pour ta majorité !"`
   * Si la valeur est `50` → `"Bon demi-siècle !"`
   * Si la valeur est `100` → `"Un siècle de vie, incroyable !"`
   * **Sinon**, le trait de soulignement (`_`) capture tous les autres âges et retourne `"Joyeux anniversaire !"`

---

