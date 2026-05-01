# Questão 4 – Reescrita de `for` em múltiplas linguagens

Código original em Java:

```java
int i, j, n = 100;
for (i = 0, j = 17; i < n; i++, j--)
  sum += i * j + 3;

# C

int i, j, n = 100;

for (i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
}

# Python:

n = 100
j = 17

for i in range(0, n):
    sum += i * j + 3
    j -= 1

# Swift:

let n = 100
var j = 17

for i in 0..<n {
    sum += i * j + 3
    j -= 1
}

# Haskell:

n = 100
sum' = sum [ i * j + 3 | (i, j) <- zip [0..n-1] [17,16..] ]

# Ruby:

n = 100
j = 17

(0...n).each do |i|
  sum += i * j + 3
  j -= 1
end
