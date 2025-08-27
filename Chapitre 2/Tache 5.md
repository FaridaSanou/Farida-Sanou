HC2T5 - Tâche 5 : et utiliser des fonctions
---

## 1️⃣ Fonction `cercleArea`

### Signature

```haskell
cercleArea :: Float -> Float
```

### Définition

L’aire d’un cercle est donnée par la formule **π × r²**.
En Haskell :

```haskell
cercleArea r = pi * r * r
```

---

## 2️⃣ Fonction `maxOfThree`

### Signature

```haskell
maxOfThree :: Int -> Int -> Int -> Int
```

### Définition

On peut utiliser la fonction intégrée `max` :

```haskell
maxOfThree x y z = max x (max y z)
```

---

## 3️⃣ Exemple 
```haskell
cercleArea :: Float -> Float
cercleArea r = pi * r * r

maxOfThree :: Int -> Int -> Int -> Int
maxOfThree x y z = max x (max y z)

-- Fonction main pour tester
main :: IO ()
main = do
    putStrLn "=== Test cercleArea ==="
    print (cercleArea 2)     -- 12.56637
    print (cercleArea 5)     -- 78.53982
    print (cercleArea 10)    -- 314.15927

    putStrLn "\n=== Test maxOfThree ==="
    print (maxOfThree 3 7 5)   -- 7
    print (maxOfThree 10 2 8)  -- 10
    print (maxOfThree 1 1 1)   -- 1
```
