HC4T1 - Tâche 1 : Définir une fonction weatherReport
```haskell
-- Définition de la fonction weatherReport
-- Cette fonction prend une chaîne (String) représentant la météo
-- et renvoie un message correspondant.

weatherReport :: String -> String
-- Cas 1 : si la météo est "sunny"
weatherReport "sunny"  = "Il fait beau et ensoleillé !"
-- Cas 2 : si la météo est "rainy"
weatherReport "rainy"  = "N'oublie pas ton parapluie !"
-- Cas 3 : si la météo est "cloudy"
weatherReport "cloudy" = "Un peu gris, mais pas de pluie pour l'instant !"
-- Cas par défaut : tout autre mot renvoie "Météo inconnue"
weatherReport _        = "Météo inconnue"

-- Exemple d'utilisation :
-- main = do
--     putStrLn (weatherReport "sunny")   -- affiche : Il fait beau et ensoleillé !
--     putStrLn (weatherReport "rainy")   -- affiche : N'oublie pas ton parapluie !
--     putStrLn (weatherReport "snowy")   -- affiche : Météo inconnue
```

---

 **Explications :**

* **`weatherReport :: String -> String`**
  → C’est la **signature de type** : la fonction prend une chaîne (`String`) et renvoie une chaîne.

* **Chaque ligne suivante** fait du **pattern matching** :

  * Si l’entrée est `"sunny"`, le résultat est `"Il fait beau et ensoleillé !"`.
  * Si c’est `"rainy"`, le résultat est `"N'oublie pas ton parapluie !"`.
  * Si c’est `"cloudy"`, le résultat est `"Un peu gris..."`.
  * Le symbole **`_`** signifie "autre cas" → tout ce qui ne correspond pas aux trois cas précédents.

---

