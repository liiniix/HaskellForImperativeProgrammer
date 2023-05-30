# Recursion

```haskell
name <args> = ... name <args'> ...

fac n =
    if n <= 1 then
        1
    else
        n * fac (n-1)
```

# Guards

```haskell
fac n
 | n <= 1    = 1
 | otherwise = n * fac (n-1)
```

# Pattern Matching

```haskell
is_zero 0 = True
is_zero _ = False
```

# Accumulators

```haskell
fac n = aux n 1
    where
      aux n acc
        | n <= 1    = acc
        | otherwise = aux (n-1) (n*acc)
```