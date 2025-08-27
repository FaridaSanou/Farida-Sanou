HC2T7 - Tâche 7 : Expressions booléennes

Écrivons des expressions booléennes quintaires :

---

## 1️⃣ `Vrai en contact &&`

```haskell
True && True    -- donne True
True && False   -- donne False
```

---

## 2️⃣ `Faux en utilisant ||`

```haskell
False || False  -- donne False
False || True   -- donne True
```

---

## 3️⃣ `Vrai en contact not`

```haskell
not True   -- donne False
not False  -- donne True
```

---

## 4️⃣ Une comparaison qui retourne `False`

```haskell
5 > 10     -- donne False
3 == 7     -- donne False
```

---

## ✅ Exemple code
main :: IO ()
main = do
    print (True && False)     -- False
    print (False || True)     -- True
    print (not True)          -- False
    print (5 > 10)            -- False
```


👉 Veux-tu que je te propose **plusieurs autres comparaisons booléennes** (par ex. `<=`, `/=`, `>=`) pour bien t’entraîner ?
