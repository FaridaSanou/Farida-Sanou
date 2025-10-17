HC4T6 - Tâche 6 : Identifier le contenu d'une liste par pattern matching


```haskell
-- Définition de la fonction whatsInsideThisList
-- Elle prend une liste de n'importe quel type ([a])
-- et retourne un message selon le nombre d'éléments.

whatsInsideThisList :: [a] -> String
-- Cas 1 : liste vide
whatsInsideThisList [] = "La liste est vide."
-- Cas 2 : liste avec un seul élément
whatsInsideThisList [_] = "La liste contient un seul élément."
-- Cas 3 : liste avec exactement deux éléments
whatsInsideThisList [_, _] = "La liste contient exactement deux éléments."
-- Cas 4 : liste avec plus de deux éléments
whatsInsideThisList (_:_:_) = "La liste contient plus de deux éléments."
```

---

 **Explications**

1. **`whatsInsideThisList :: [a] -> String`**

   * La fonction prend une **liste de n’importe quel type (`[a]`)** et renvoie une **chaîne (`String`)**.

2. **Pattern matching sur les listes :**

   * `[]` → liste vide.
   * `[_]` → une liste avec **un seul élément** (le `_` signifie qu’on ne se préoccupe pas de la valeur).
   * `[_, _]` → liste avec **exactement deux éléments**.
   * `(_:_:_)` → liste avec **au moins deux éléments** ; le `_` ignore les valeurs, et `:` est le constructeur de liste.

     * Les deux premiers `_` représentent les deux premiers éléments.
     * Le troisième `_` avec `:` signifie “et le reste de la liste”.

---


