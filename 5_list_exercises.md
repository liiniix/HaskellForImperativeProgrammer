# Exercise #1

### Create a function `elem` that returns `True` if an element is in a given list and returns `False` otherwise

```haskell
elem :: (Eq a) => a -> [a] -> Bool

elem a (x:xs) =
 | xs == []: False
 | a == x : True
 | elem a xs

elem _ [] = False
elem e (x:xs) = (e == x) || (elem e xs)
```

# Exercise #2

### Create a function `nub` that removes all duplicates from a given list

```haskell
nub :: (Eq a) => [a] -> [a]
nub [] = []
nub (x:xs)
 | x `elem` xs = nub xs
 | otherwise   = x : nub xs
```

# Exercise #3

### create a function `isAsc` that returns `True` if the list given to it is a list of ascending order

```haskell
isAsc :: [Int] -> Bool
isAsc [] = True
isAsc [x] = True
isAsc (x : y : xs) = x <= y && isAsc (y:xs)
```

# Exercise #4

### Create a function `hasPath` that determines if a path from one node to another exit within a directed graph

```haskell
hasPath :: [(Int, Int)] -> Int -> Int -> Bool
hasPath [] x y = True
hasPath xs x y
 | x == y = return True
 | otherwise =
    let xs' = [ (n, m) | (n, m) <- xs , n /= x] in
                or [hasPath xs' m y | (n, m) <- xs, n == x]