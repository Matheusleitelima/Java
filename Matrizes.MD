# Arrays (Matrizes) em Java

Arrays são estruturas utilizadas para armazenar múltiplos valores do mesmo tipo em uma única variável.

---

# Declarando Arrays

Para declarar um array, utilize colchetes `[]` após o tipo da variável.

```java
String[] cars;
```

---

# Inicializando Arrays

Você pode criar e preencher o array ao mesmo tempo utilizando chaves `{}`.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

### Array de números inteiros

```java
int[] myNum = {10, 20, 30, 40};
```

---

# Acessando Elementos

Os elementos são acessados através de índices.

> Em Java, os índices começam em 0.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

System.out.println(cars[0]);
```

### Saída

```text
Volvo
```

### Índices

| Índice | Elemento |
|---------|----------|
| 0 | Volvo |
| 1 | BMW |
| 2 | Ford |
| 3 | Mazda |

---

# Alterando um Elemento

Você pode modificar um valor utilizando seu índice.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

cars[0] = "Opel";

System.out.println(cars[0]);
```

### Saída

```text
Opel
```

---

# Comprimento do Array

A propriedade `.length` retorna a quantidade de elementos do array.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

System.out.println(cars.length);
```

### Saída

```text
4
```

---

# Criando Arrays com `new`

Também é possível criar um array vazio informando seu tamanho.

```java
String[] cars = new String[4];
```

Depois, basta preencher as posições:

```java
cars[0] = "Volvo";
cars[1] = "BMW";
cars[2] = "Ford";
cars[3] = "Mazda";

System.out.println(cars[0]);
```

### Saída

```text
Volvo
```

---

# Percorrendo Arrays com `for`

Você pode utilizar um loop `for` junto com a propriedade `.length`.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (int i = 0; i < cars.length; i++) {
    System.out.println(cars[i]);
}
```

### Saída

```text
Volvo
BMW
Ford
Mazda
```

---

# Percorrendo Arrays com `for-each`

O `for-each` é uma forma mais simples de percorrer arrays.

## Sintaxe

```java
for (tipo variavel : array) {
    // código
}
```

## Exemplo

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (String car : cars) {
    System.out.println(car);
}
```

### Saída

```text
Volvo
BMW
Ford
Mazda
```

---

# Arrays Multidimensionais

Um array multidimensional é um array que contém outros arrays.

É muito utilizado para representar tabelas, matrizes, planilhas e jogos.

## Exemplo

```java
int[][] myNumbers = {
    {1, 4, 2},
    {3, 6, 8}
};
```

Visualmente:

| Linha | Valores |
|---------|----------|
| 0 | 1, 4, 2 |
| 1 | 3, 6, 8 |

---

# Acessando Elementos de uma Matriz

Para acessar um elemento, informe:

- Primeiro índice → Linha
- Segundo índice → Coluna

```java
int[][] myNumbers = {
    {1, 4, 2},
    {3, 6, 8}
};

System.out.println(myNumbers[1][2]);
```

### Saída

```text
8
```

### Representação

```text
[1][2]

Linha 1 -> {3, 6, 8}
             0  1  2
```

---

# Alterando Valores

```java
int[][] myNumbers = {
    {1, 4, 2},
    {3, 6, 8}
};

myNumbers[1][2] = 9;

System.out.println(myNumbers[1][2]);
```

### Saída

```text
9
```

---

# Percorrendo Matrizes Multidimensionais

Normalmente utilizamos loops aninhados.

```java
int[][] myNumbers = {
    {1, 4, 2},
    {3, 6, 8, 5, 2}
};

for (int row = 0; row < myNumbers.length; row++) {

    for (int col = 0; col < myNumbers[row].length; col++) {

        System.out.println(
            "myNumbers[" + row + "][" + col + "] = "
            + myNumbers[row][col]
        );

    }
}
```

### Saída

```text
myNumbers[0][0] = 1
myNumbers[0][1] = 4
myNumbers[0][2] = 2
myNumbers[1][0] = 3
myNumbers[1][1] = 6
myNumbers[1][2] = 8
myNumbers[1][3] = 5
myNumbers[1][4] = 2
```

---

# Percorrendo Matrizes com `for-each`

Uma alternativa mais legível é utilizar `for-each` nos dois níveis.

```java
int[][] myNumbers = {
    {1, 4, 2},
    {3, 6, 8, 5, 2}
};

for (int[] row : myNumbers) {

    for (int num : row) {

        System.out.println(num);

    }
}
```

### Saída

```text
1
4
2
3
6
8
5
2
```

---

# Resumo

| Conceito | Descrição |
|-----------|------------|
| `tipo[] nome` | Declara um array |
| `{}` | Inicializa um array |
| `array[indice]` | Acessa um elemento |
| `array.length` | Retorna o tamanho do array |
| `new Tipo[tamanho]` | Cria um array vazio |
| `for` | Percorre arrays usando índices |
| `for-each` | Percorre arrays de forma simplificada |
| `tipo[][]` | Cria um array multidimensional |
| `[linha][coluna]` | Acessa elementos de uma matriz |

---
