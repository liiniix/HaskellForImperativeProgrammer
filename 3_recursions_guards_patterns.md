# Recursion

```haskell
name <args> = ... name <args'> ...

fac n =
    if n <=1 then
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