HC4T5 - Tâche 5 : Ajouter un cas générique avec un message personnalisé

---


```haskell
-- Définition de la fonction specialBirthday
-- Elle prend un âge (Int) et retourne un message adapté.

specialBirthday :: Int -> String
-- Cas 1 : âge = 1
specialBirthday 1 = "Joyeux 1er anniversaire !"
-- Cas 2 : âge = 18
specialBirthday 18 = "Félicitations pour ta majorité !"
-- Cas 3 : âge = 50
specialBirthday 50 = "Bon demi-siècle !"
-- Cas 4 : âge = 100
specialBirthday 100 = "Un siècle de vie, incroyable !"
-- Cas générique : tout autre âge
specialBirthday age = "Joyeux " ++ show age ++ "e anniversaire !"
```

---

 **Explications :**

1. **`specialBirthday :: Int -> String`**
   → La fonction prend un entier (`Int`) et renvoie une chaîne de caractères (`String`).

2. **Les cas spécifiques** sont toujours traités en premier (1, 18, 50, 100).
   → Si la valeur correspond à l’un de ces âges, le message fixe est renvoyé.

3. **Le dernier cas (`specialBirthday age`)** capture tous les autres âges.

   * Ici, `age` est une variable qui contient la valeur saisie.
   * L’expression `show age` convertit l’entier en texte.
   * L’opérateur `++` sert à **concaténer** des chaînes en Haskell.

    Exemple : si `age = 25`,
   alors `"Joyeux " ++ show 25 ++ "e anniversaire !"` devient
   `"Joyeux 25e anniversaire !"`

---

