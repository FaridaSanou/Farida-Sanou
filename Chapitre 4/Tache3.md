HC4T4 - Tâche 4 : Réécrire specialBirthday avec le pattern matching

```haskell
-- Définition de la fonction gradeComment
-- Cette fonction prend une note entière (Int)
-- et retourne un message selon la performance de l’étudiant.

gradeComment :: Int -> String
-- Cas 1 : entre 90 et 100
gradeComment note
    | note >= 90 && note <= 100 = "Excellent !"
-- Cas 2 : entre 70 et 89
    | note >= 70 && note <= 89  = "Bon travail !"
-- Cas 3 : entre 50 et 69
    | note >= 50 && note <= 69  = "Tu as réussi."
-- Cas 4 : entre 0 et 49
    | note >= 0  && note <= 49  = "Peut mieux faire."
-- Cas 5 : toute autre valeur (en dehors de 0 à 100)
    | otherwise                 = "Note invalide."
```

---

  **Explications **

1. **`gradeComment :: Int -> String`**
   → La fonction prend un entier (`Int`) et renvoie une chaîne (`String`).

2. **`gradeComment note`**
   → On définit une fonction qui reçoit une variable `note`.

3. **Les gardes (`|`)**
   En Haskell, les gardes permettent de tester plusieurs conditions de manière lisible (comme des "si / sinon si").

   * `| note >= 90 && note <= 100` → renvoie `"Excellent !"`
   * `| note >= 70 && note <= 89`  → renvoie `"Bon travail !"`
   * `| note >= 50 && note <= 69`  → renvoie `"Tu as réussi."`
   * `| note >= 0 && note <= 49`   → renvoie `"Peut mieux faire."`
   * `| otherwise` → correspond au cas par défaut (équivalent de “sinon”).

---





```


