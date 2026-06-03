# Estruturas Condicionais em Java

As estruturas condicionais permitem que o programa tome decisões com base em condições.

---

## If

O `if` executa um bloco de código apenas se a condição for verdadeira.

### Exemplo

```java
boolean isRaining = true;

if (isRaining) {
    System.out.println("Bring an umbrella!");
}
```

---

## Operadores de Comparação

| Operador | Significado |
|-----------|-------------|
| `<` | Menor que |
| `<=` | Menor ou igual a |
| `>` | Maior que |
| `>=` | Maior ou igual a |
| `==` | Igual a |
| `!=` | Diferente de |

### Exemplo

```java
int idade = 18;

if (idade >= 18) {
    System.out.println("Maior de idade");
}
```

---

## If e Else

O `else` é executado quando a condição do `if` for falsa.

### Exemplo

```java
boolean isRaining = false;

if (isRaining) {
    System.out.println("Bring an umbrella!");
} else {
    System.out.println("No rain today, no need for an umbrella!");
}
```

---

## Else If

O `else if` permite testar uma nova condição caso a anterior seja falsa.

### Exemplo

```java
int nota = 75;

if (nota >= 90) {
    System.out.println("Excelente");
} else if (nota >= 70) {
    System.out.println("Aprovado");
} else {
    System.out.println("Reprovado");
}
```

### Estrutura Geral

```java
if (condition1) {
    // Executa se condition1 for verdadeira
} else if (condition2) {
    // Executa se condition1 for falsa
    // e condition2 for verdadeira
} else {
    // Executa se todas as condições forem falsas
}
```

---

## If Aninhado (Nested If)

Um `if` pode ser colocado dentro de outro `if`.

### Exemplo

```java
if (condition1) {
    // Executa se condition1 for verdadeira

    if (condition2) {
        // Executa se condition1 e condition2 forem verdadeiras
    }
}
```

### Exemplo Prático

```java
int idade = 20;
boolean possuiCarteira = true;

if (idade >= 18) {
    if (possuiCarteira) {
        System.out.println("Pode dirigir");
    }
}
```

---

## Switch

O `switch` é utilizado quando há várias opções possíveis para uma mesma variável.

### Exemplo

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
