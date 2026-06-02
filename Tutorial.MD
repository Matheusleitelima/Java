# 📚 Guia Básico de Java

## Estrutura Principal

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World");
    }
}
```

### Explicação

- `public class Main` → Cria uma classe chamada Main.
- `public static void main(String[] args)` → Método principal do programa.
- `System.out.println()` → Exibe informações na tela.

---

# Comentários em Java

## Comentário de uma linha

```java
// Isso é um comentário
```

## Comentário de múltiplas linhas

```java
/*
Isso é um comentário
de várias linhas
*/
```

---

# Tipos de Dados Primitivos

```java
int myNum = 5;
float myFloatNum = 5.99f;
char myLetter = 'D';
boolean myBool = true;
String myText = "Hello";
```

| Tipo | Descrição |
|--------|-----------|
| byte | Números inteiros de -128 a 127 |
| short | Números inteiros de -32.768 a 32.767 |
| int | Números inteiros de -2.147.483.648 a 2.147.483.647 |
| long | Números inteiros muito grandes |
| float | Números decimais (6 a 7 casas de precisão) |
| double | Números decimais (15 a 16 casas de precisão) |
| boolean | true ou false |
| char | Um único caractere |

---

# Declaração de Variáveis

## Sintaxe

```java
tipo nomeVariavel = valor;
```

### Exemplos

```java
String nome = "John";
int idade = 19;
float altura = 1.75f;
char sexo = 'M';
boolean ativo = true;
```

### Exibindo variável

```java
String nome = "John";
System.out.println(nome);
```

---

# Constantes

Variáveis que não podem ser alteradas.

```java
final int idade = 19;
```

---

# Tipos Não Primitivos

São chamados de **tipos de referência**, pois apontam para objetos.

## Exemplos

- String
- Arrays
- Classes
- Objetos

## Diferenças

### Tipos Primitivos

- Já existem na linguagem.
- Começam com letra minúscula.
- Sempre possuem valor.

Exemplo:

```java
int idade = 19;
```

### Tipos Não Primitivos

- Criados pelo programador (exceto String).
- Começam com letra maiúscula.
- Podem ser `null`.
- Possuem métodos.

Exemplo:

```java
String nome = "Matheus";
```

---

# Conversão de Tipos (Casting)

## Conversão Automática (Widening)

```java
int myInt = 9;
double myDouble = myInt;
```

Resultado:

```java
9 → 9.0
```

## Conversão Manual (Narrowing)

```java
double myDouble = 9.78;
int myInt = (int) myDouble;
```

Resultado:

```java
9.78 → 9
```

---

# Operadores Aritméticos

| Operador | Descrição |
|-----------|-----------|
| + | Soma |
| - | Subtração |
| * | Multiplicação |
| / | Divisão |
| % | Resto da divisão |
| ++ | Incremento |
| -- | Decremento |

## Exemplos

```java
int x = 10;
int y = 5;

System.out.println(x + y);
System.out.println(x - y);
System.out.println(x * y);
System.out.println(x / y);
System.out.println(x % y);
```

---

# Incremento e Decremento

```java
int x = 5;

++x;
System.out.println(x);
```

Saída:

```java
6
```

---

# Operadores de Atribuição

| Operador | Exemplo | Equivale a |
|-----------|----------|------------|
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| %= | x %= 3 | x = x % 3 |

---

# Operadores de Comparação

| Operador | Significado |
|-----------|-------------|
| == | Igual |
| != | Diferente |
| > | Maior |
| < | Menor |
| >= | Maior ou igual |
| <= | Menor ou igual |

## Exemplo

```java
int x = 10;
int y = 5;

System.out.println(x > y);
```

Resultado:

```java
true
```

---

# Operadores Lógicos

| Operador | Nome |
|-----------|------|
| && | AND |
| \|\| | OR |
| ! | NOT |

## Exemplos

### AND

```java
x < 5 && x < 10
```

### OR

```java
x < 5 || x < 4
```

### NOT

```java
!(x < 5 && x < 10)
```

---

# Ordem das Operações

1. `()`
2. `*`, `/`, `%`
3. `+`, `-`
4. `>`, `<`, `>=`, `<=`
5. `==`, `!=`
6. `&&`
7. `||`
8. `=`

---

# Strings

## Tamanho da String

```java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

System.out.println(txt.length());
```

---

## Converter para Maiúsculas

```java
String nome = "matheus";

System.out.println(nome.toUpperCase());
```

Resultado:

```java
MATHEUS
```

---

## Converter para Minúsculas

```java
String nome = "MATHEUS";

System.out.println(nome.toLowerCase());
```

Resultado:

```java
matheus
```

---

# Concatenação de Strings

## Usando +

```java
String firstName = "John";
String lastName = "Doe";

System.out.println(firstName + " " + lastName);
```

Resultado:

```java
John Doe
```

---

## Usando concat()

```java
String firstName = "John ";
String lastName = "Doe";

System.out.println(firstName.concat(lastName));
```

Resultado:

```java
John Doe
```

---

# Matemática em Java (Classe Math)

## Maior valor

```java
Math.max(x, y);
```

---

## Menor valor

```java
Math.min(x, y);
```

---

## Raiz quadrada

```java
Math.sqrt(x);
```

---

## Valor absoluto

```java
Math.abs(x);
```

---

## Potência

```java
Math.pow(x, y);
```

Exemplo:

```java
Math.pow(2, 3);
```

Resultado:

```java
8
```

---

