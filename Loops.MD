# Loops e Estruturas de Repetição em Java

Os loops permitem executar um bloco de código repetidamente enquanto uma condição for verdadeira ou até que um critério seja atingido.

---

# Switch

A estrutura `switch` é utilizada para selecionar entre vários blocos de código com base no valor de uma expressão.

## Sintaxe

```java
switch(expression) {
    case x:
        // código
        break;

    case y:
        // código
        break;

    default:
        // código
}
```

## Exemplo

```java
int dia = 3;

switch (dia) {
    case 1:
        System.out.println("Domingo");
        break;

    case 2:
        System.out.println("Segunda-feira");
        break;

    case 3:
        System.out.println("Terça-feira");
        break;

    default:
        System.out.println("Dia inválido");
}
```

---

# Loop While

O `while` executa um bloco de código enquanto a condição for verdadeira.

## Sintaxe

```java
while (condition) {
    // código
}
```

## Exemplo

```java
int i = 0;

while (i < 5) {
    System.out.println(i);
    i++;
}
```

### Saída

```text
0
1
2
3
4
```

---

# Loop Do/While

O `do/while` é uma variação do `while`.

A principal diferença é que o bloco de código será executado pelo menos uma vez, mesmo que a condição seja falsa.

## Sintaxe

```java
do {
    // código
} while (condition);
```

## Exemplo

```java
int i = 0;

do {
    System.out.println(i);
    i++;
} while (i < 5);
```

### Saída

```text
0
1
2
3
4
```

---

# Loop For

O `for` é utilizado quando sabemos quantas vezes o bloco de código deve ser executado.

## Sintaxe

```java
for (inicialização; condição; incremento) {
    // código
}
```

### Componentes

- **Inicialização:** executada apenas uma vez.
- **Condição:** define até quando o loop será executado.
- **Incremento:** executado ao final de cada repetição.

## Exemplo

```java
for (int i = 0; i <= 10; i += 2) {
    System.out.println(i);
}
```

### Saída

```text
0
2
4
6
8
10
```

---

# Loops Aninhados

Um loop pode ser colocado dentro de outro loop.

O loop interno executa completamente a cada repetição do loop externo.

## Exemplo

```java
for (int i = 1; i <= 2; i++) {
    System.out.println("Outer: " + i);

    for (int j = 1; j <= 3; j++) {
        System.out.println(" Inner: " + j);
    }
}
```

### Saída

```text
Outer: 1
 Inner: 1
 Inner: 2
 Inner: 3
Outer: 2
 Inner: 1
 Inner: 2
 Inner: 3
```

---

# Loop For-Each

O `for-each` é utilizado para percorrer arrays e coleções de forma simplificada.

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

# Break

A instrução `break` interrompe imediatamente a execução de um loop.

## Exemplo

```java
for (int i = 0; i < 10; i++) {
    if (i == 4) {
        break;
    }

    System.out.println(i);
}
```

### Saída

```text
0
1
2
3
```

---

# Continue

A instrução `continue` interrompe apenas a iteração atual e passa para a próxima.

## Exemplo

```java
for (int i = 0; i < 10; i++) {
    if (i == 4) {
        continue;
    }

    System.out.println(i);
}
```

### Saída

```text
0
1
2
3
5
6
7
8
9
```

---

# Resumo

| Estrutura | Finalidade |
|------------|------------|
| `switch` | Escolher entre várias opções |
| `while` | Repetir enquanto a condição for verdadeira |
| `do/while` | Executar pelo menos uma vez e depois testar a condição |
| `for` | Repetir um número conhecido de vezes |
| `for-each` | Percorrer arrays e coleções |
| `break` | Encerrar o loop imediatamente |
| `continue` | Pular a iteração atual |

---

## Quando usar cada loop?

- Use **for** quando souber quantas repetições serão necessárias.
- Use **while** quando não souber exatamente quantas repetições ocorrerão.
- Use **do/while** quando precisar executar o código pelo menos uma vez.
- Use **for-each** para percorrer arrays e coleções de forma mais simples.
