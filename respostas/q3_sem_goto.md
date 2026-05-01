# Questão 3 – Reescrita sem `goto` e sem `break`

Código original em C:

```c
j = -3;
for (i = 0; i < 3; i++) {
  switch (j + 2) {
    case 3:
    case 2: j--; break;
    case 0: j += 2; break;
    default: j = 0;
  }
  if (j > 0) break;
  j = 3 - i;
}

# Java:

int j = -3;
int i = 0;
boolean continuar = true;

while (i < 3 && continuar) {

    int valor = j + 2;

    if (valor == 3 || valor == 2) {
        j--;
    } else if (valor == 0) {
        j += 2;
    } else {
        j = 0;
    }

    if (j > 0) {
        continuar = false;
    } else {
        j = 3 - i;
        i++;
    }
}

# Python:

j = -3
i = 0
continuar = True

while i < 3 and continuar:
    valor = j + 2

    if valor == 3 or valor == 2:
        j -= 1
    elif valor == 0:
        j += 2
    else:
        j = 0

    if j > 0:
        continuar = False
    else:
        j = 3 - i
        i += 1

# Swift:

var j = -3
var i = 0
var continuar = true

while i < 3 && continuar {

    let valor = j + 2

    if valor == 3 || valor == 2 {
        j -= 1
    } else if valor == 0 {
        j += 2
    } else {
        j = 0
    }

    if j > 0 {
        continuar = false
    } else {
        j = 3 - i
        i += 1
    }
}
