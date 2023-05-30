# Lists

```haskell
[1, 2, 3, 4, 5, 6]
[1, 2, 3, 4, 5, 6] :: [Integer]

[]
x:xs

1 : 2 : 3 : 4 : 5 : 6 : []
```

# Generating a List Ascending from a Number to Another Number

```haskell
asc :: Int -> Int -> [Int]
asc n m
 | n > m   = []
 | n == m  = [m]
 | n < m   = n : asc (n+1) m


asc 1 3
 => [1, 2, 3]
```

# Functions on Lists

```haskell
import Data.List

head :: [a] -> a
head [1, 2, 3, 4]
  => 1

tail :: [a] -> a
tail [1, 2, 3, 4]
  => [2, 3, 4]

 length :: [a] -> Int
 length [1, 2, 3, 4]
  => 4

init :: [a] -> [a]
init [1, 2, 3, 4]
  => [1, 2, 3, 4]

null :: [a] -> Bool
null []
  => True

null [1, 2, 3, 4]
  => False
```