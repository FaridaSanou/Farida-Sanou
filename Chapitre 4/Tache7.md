HC4T7 - Tâche 7 : Ignorer des éléments dans une liste

```haskell
-- Définition de la fonction firstAndThird
-- Elle prend une liste de n'importe quel type ([a])
-- et renvoie une paire contenant le premier et le troisième élément.

firstAndThird :: [a] -> (a, a)
-- Cas général : liste avec au moins trois éléments
firstAndThird (x:_:z:_) = (x, z)
-- Cas où il y a moins de trois éléments : erreur ou message
firstAndThird _ = error "La liste doit contenir au moins trois éléments."
```

---

 **Explications**

1. **`firstAndThird :: [a] -> (a, a)`**

   * La fonction prend une **liste de n’importe quel type (`[a]`)**.
   * Elle renvoie **une paire `(a, a)`** contenant le premier et le troisième élément.

2. **Pattern matching `(x:_:z:_)`**

   * `x` → premier élément
   * `_` → **on ignore le deuxième élément**
   * `z` → troisième élément
   * `_` → **on ignore le reste de la liste**, peu importe sa longueur.

3. **Cas `_`**

   * Si la liste a moins de trois éléments, on renvoie une erreur avec `error`.

---

 **Exemples de test dans GHCi**

```haskell
firstAndThird [1,2,3,4,5]   -- (1,3)
firstAndThird ["a","b","c"] -- ("a","c")
firstAndThird [10,20]       -- Erreur : La liste doit contenir au moins trois éléments
```

---

