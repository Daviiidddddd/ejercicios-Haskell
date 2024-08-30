# Ejercicios Haskell

## Integrantes: 
## David Castellanos
## Santiago Cespedes
## Diana Acosta

## 1. Ejercicio 1

```haskell
let reverseList [] = []; reverseList (x:xs) = reverseList xs ++ [x]
reverseList [1, 2, 3, 4, 5]
```

## 2. Ejercicio 2

 ```haskell
 let isPalindrome :: (Eq a) => [a] -> Bool; isPalindrome xs = xs == reverse xs
 isPalindrome "reconocer"
```

## 3. Ejercicio 3

```haskell
 let sumList :: [Int] -> Int; sumList [] = 0; sumList (x:xs) = x + sumList xs 
 sumList [1,2,4,5,6]
```

## 4. Ejercicio 4

```haskell
let maxList :: [Int] -> Int; maxList [] = error "Lista vacía"; maxList [x] = x; maxList (x:xs) = max x (maxList x)
maxList [1,2,4,10,100]
```

## 5. Ejercicio 5

```haskell
let fibonacci :: Int -> Int; fibonacci 0=0; fibonacci 1=1; fibonacci n = fibonacci (n-1) + fibonacci (n-2)
fibonacci 6
```

## 6. Ejercicio 6

```haskell
let factorialFoldl :: Int -> Int; factorialFoldl n = foldl (*) 1 [1..n]
factorialFoldl 6
```

## 7. Ejercicio 7

```haskell
let filterEvens :: [Int] -> [Int]; filterEvens xs = filter even xs
filterEvens [1,2,4,6,11,110]
```

## 8. Ejercicio 8

```haskell
let concatLists :: [a] -> [a] -> [a]; concatLists [] ys = ys; concatLists (x:xs) ys = x : concatLists xs ys
concatLists [1,2,3] [7,8,9]
```

## 9. Ejercicio 9

```haskell
let invertTuples :: [(a, b)] -> [(b, a)]; invertTuples xs = [(y, x) | (x, y) <- xs]
invertTuples [(10, "Hola"), (20, "Mundo")]
```

## 10. Ejercicio 10

```haskell
let applyFunction :: (a -> b) -> [a] -> [b]; applyFunction f xs = map f xs
applyFunction (*2) [1, 2, 3, 4]
```

## 11. Ejercicio 11

```haskell
let productList :: [Int] -> Int; productList [] = 1; productList (x:xs) = x * productList xs
productList [1, 2, 3, 4, 10]
```

## 12. Ejercicio 12

```haskell
let removeDuplicates :: (Eq a) => [a] -> [a]; removeDuplicates [] = []; removeDuplicates (x:xs) | x `elem` xs = removeDuplicates xs | otherwise = x : removeDuplicates xs
removeDuplicates [1, 2, 3, 2, 4, 1, 10, 10]
```

## 13. Ejercicio 13

```haskell
let average :: [Double] -> Double; average xs = sum xs / fromIntegral (length xs)
average [1.0, 2.0, 3.0, 4.0, 5.0, 6.5]
```

## 14. Ejercicio 14

```haskell
let mergeSorted :: Ord a => [a] -> [a] -> [a]; mergeSorted [] ys = ys; mergeSorted xs [] = xs; mergeSorted (x:xs) (y:ys) | x <= y = x : mergeSorted xs (y:ys) | otherwise = y : mergeSorted (x:xs) ys
mergeSorted [1, 3, 5] [2, 4, 6]
```

## 15. Ejercicio 15

```haskell
let removeNegatives :: [Int] -> [Int]; removeNegatives xs = filter (>= 0) xs
removeNegatives [1, -2, 3, -4, 5]
```
