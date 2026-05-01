# Questão 1 – Loops (sem goto)

```text
k = (j + 13) / 27
loop:
if k > 10 then goto out
k = k + 1
i = 3 * k - 1
goto loop
out: ...

# Java

k = (j + 13) / 27;

while (k <= 10) {
    k = k + 1;
    i = 3 * k - 1;
}

// out: ...

# Python

k = (j + 13) // 27

while k <= 10:
    k = k + 1
    i = 3 * k - 1

# out: ...

# Haskell

loop :: Int -> Int -> (Int, Int)
loop j i =
  let k0 = (j + 13) `div` 27
  in go k0 i
  where
    go k i
      | k > 10    = (k, i)
      | otherwise =
          let k' = k + 1
              i' = 3 * k' - 1
          in go k' i'

# Swift

var k = (j + 13) / 27

while k <= 10 {
    k = k + 1
    i = 3 * k - 1
}

// out: ...
