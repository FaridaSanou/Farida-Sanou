HC4T2 - Tâche 2 : Définir une fonction dayType
---

```haskell
-- Définition de la fonction dayType
-- Cette fonction prend un jour de la semaine (String)
-- et indique s’il s’agit d’un jour de semaine, d’un week-end ou d’un jour invalide.

dayType :: String -> String
-- Cas 1 : si le jour est "Saturday" ou "Sunday"
dayType "Saturday" = "C'est le week-end !"
dayType "Sunday"   = "C'est le week-end !"

-- Cas 2 : si le jour est un jour de semaine
dayType "Monday"    = "C'est un jour de semaine."
dayType "Tuesday"   = "C'est un jour de semaine."
dayType "Wednesday" = "C'est un jour de semaine."
dayType "Thursday"  = "C'est un jour de semaine."
dayType "Friday"    = "C'est un jour de semaine."

-- Cas 3 : pour tout autre mot
dayType _ = "Jour invalide"

-- Exemple d'utilisation :
-- main :: IO ()
-- main = do
--     putStrLn (dayType "Monday")    -- C'est un jour de semaine.
--     putStrLn (dayType "Sunday")    -- C'est le week-end !
--     putStrLn (dayType "Holiday")   -- Jour invalide
```

---

 **Explications :**

1. **`dayType :: String -> String`**
   → La signature de type indique que la fonction prend une chaîne (`String`) et renvoie une chaîne.

2. **Pattern matching :**

   * Si le mot correspond à `"Saturday"` ou `"Sunday"` → on affiche `"C'est le week-end !"`.
   * Si c’est un des cinq autres jours de la semaine → on renvoie `"C'est un jour de semaine."`.
   * Sinon, le caractère **`_`** capture tout le reste → `"Jour invalide"`.

---



Souhaites-tu que je te montre une **version simplifiée** (avec moins de répétition) en utilisant des **listes et une condition** ?
