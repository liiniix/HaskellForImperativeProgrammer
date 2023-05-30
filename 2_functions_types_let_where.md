# Functions (Definition)

```haskell
name arg1, arg2, ... , argn = <expr>
```

# Functions (Examples)

```haskell
in_range_between_min_max min max x = 
                    x >= min && x <= max

in_range_between_min_max 2 6 3
                    => True

in_range_between_min_max 5 6 3
                    => False 
```

# Types (Basics)

```haskell
name :: <type>
```

```haskell
x :: Integer
x = 1

y :: Bool
y = True

z :: Float
z = 1.2
```

# Types (Functions)

```haskell
in_range_between_min_max :: Integer -> Integer -> Integer -> Bool
in_range_between_min_max min max x = x >= min && x <= max

in_range_between_min_max .1 .4 .6 <- Type Error
in_range_between_min_max 1 4 6 <- Correct
```

# Functions (let)

```haskell
in_range_between_min_max min max x =
                in_lower_bound = min <= x;
                in_upper_bound = x <= max;
                return (in_lower_bound && in_upper_bound);

in_range_between_min_max min max x =
                let in_lower_bound = min <= x
                    in_upper_bound = x <= max
                in
                in_lower_bound && in_upper_bound

in_range_between_min_max min max x = in_lower_bound && in_upper_bound
                where
                    in_lower_bound = min <= x
                    in_upper_bound = x <= max                
```