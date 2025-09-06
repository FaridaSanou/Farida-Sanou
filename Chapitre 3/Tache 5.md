HC3T5 - Tâche 5 : Déterminer le type d'un triangle avec des gardes


Ecrivons une fonction qui classe un triangle selon ses côtés. En Haskell, on utilise les gardes (`|`)** pour tester des conditions de manière claire.

---

# 1. Les types

```haskell
triangleType :: Int -> Int -> Int -> String
```

* La fonction prend **trois entiers** (les longueurs des côtés).
* Elle retourne un **String** (le type du triangle).

---

# 2. Les règles mathématiques

Un triangle valide doit respecter la règle des inégalités :

* Chaque côté doit être strictement inférieur à la somme des deux autres.
  Sinon, ce n’est pas un triangle.

Ensuite, on distingue :

* Équilatéral : $a = b = c$
* Isocèle : deux côtés égaux
* Scalène : tous les côtés différents

---

# 3. Implémentation avec gardes

```haskell
triangleType :: Int -> Int -> Int -> String
triangleType a b c
    | a + b <= c || a + c <= b || b + c <= a = "Pas un triangle"
    | a == b && b == c                       = "Équilatéral"
    | a == b || b == c || a == c             = "Isocèle"
    | otherwise                              = "Scalène"
```

---

# 4. Explication ligne par ligne

* `a + b <= c || a + c <= b || b + c <= a`
  si un côté est supérieur ou égal à la somme des deux autres → impossible de former un triangle → on retourne `"Pas un triangle"`.

* `a == b && b == c`
   si les trois côtés sont égaux → triangle Équilatéral.

* `a == b || b == c || a == c`
   si au moins deux côtés sont égaux → triangle Isocèle

* `otherwise`
   tous les autres cas → triangle Scalène.

---

# 5. Exemple d’utilisation

```haskell
main :: IO ()
main = do
    print (triangleType 3 3 3)   -- "Équilatéral"
    print (triangleType 5 5 8)   -- "Isocèle"
    print (triangleType 6 7 8)   -- "Scalène"
    print (triangleType 2 2 5)   -- "Pas un triangle"
```

---


👉 Veux-tu que je te fasse aussi un **schéma visuel** (comme un petit tableau ou diagramme) pour montrer la logique de décision étape par étape ?
