HC2T4 - Tâche 4 : Notation préfixe et infixe
---

## 1️⃣ Notation **préfixe**

En Haskell, **préfixe** signifie que **le nom de la fonction vient avant ses arguments** :

### Exemples:

1. `5 et 3`
   Si `et` est une fonction de somme (`+`) ou d’addition, la notation préfixe serait :

```haskell
(+) 5 3
```

2. `10 et 4`

```haskell
(+) 10 4
```

3. `Vrai et faux`
   Si `et` est la fonction logique `&&` :

```haskell
(&&) True False
```

> ✅ Remarque : en notation préfixe, **les opérateurs sont entourés de parenthèses** pour être utilisés comme fonctions normales.

---

## 2️⃣ Notation **infixe**

En **notation infixe**, les opérateurs ou fonctions se placent **entre leurs deux arguments** :

### Exemples :

1. `7 2`
   Si c’est l’addition :

```haskell
7 + 2
```

2. `6 5`

```haskell
6 + 5
```

3. `Vrai faux`
   Si c’est `&&` :

```haskell
True && False
```

> ✅ Remarque : tout opérateur ou fonction binaire peut être utilisé en **infixe** si on ne met pas de parenthèses autour.

---


