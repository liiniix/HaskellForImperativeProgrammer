# Declarative vs. Imperative

### Declarative
```haskell
sum [] = 0
sum [x:xs] = x + sum(xs)

or,

sum = foldr (+) 0
```

### Imperative

```cpp
int sum(int *arr, int length)
{
    int summation = 0;
    for(int i=0; i<length; ++i)
    {
        summation += arr[i];
    }

    return summation;
}
```

# Lazy vs. Strict

### Declarative
```haskell
func arg = 
        let x = func1 arg
            y = func2 arg
            z = func3 arg
        in
        if z then x else y
```

### Imperative

```cpp
int func(int arg)
{
    int x = func1(arg);
    int y = func2(arg);
    int z = func3(arg);

    if(z){
        return x;
    } else{
        return y;
    }
}
```