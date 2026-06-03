# Métodos em Java

Métodos são blocos de código reutilizáveis que executam uma tarefa específica.

Eles ajudam a organizar o código, evitar repetição e tornar os programas mais fáceis de manter.

> Em outras linguagens, métodos também são conhecidos como **funções**.

---

# O que é um Método?

Um método é um bloco de código que só será executado quando for chamado.

## Estrutura Básica

```java
public class Main {

    static void myMethod() {
        // código a ser executado
    }

}
```

### Componentes

| Parte | Descrição |
|---------|-----------|
| `static` | Permite chamar o método sem criar um objeto |
| `void` | Indica que o método não retorna valor |
| `myMethod()` | Nome do método |
| `{}` | Bloco de código do método |

---

# Criando um Método

```java
public class Main {

    static void myMethod() {
        System.out.println("I just got executed!");
    }

}
```

Neste exemplo, o método apenas imprime uma mensagem.

---

# Chamando um Método

Para executar um método, basta chamá-lo pelo nome.

```java
public class Main {

    static void myMethod() {
        System.out.println("I just got executed!");
    }

    public static void main(String[] args) {
        myMethod();
    }

}
```

### Saída

```text
I just got executed!
```

---

# Parâmetros

Parâmetros permitem enviar informações para um método.

## Exemplo

```java
public class Main {

    static void myMethod(String fname) {
        System.out.println(fname + " Refsnes");
    }

    public static void main(String[] args) {

        myMethod("Liam");
        myMethod("Jenny");
        myMethod("Anja");

    }

}
```

### Saída

```text
Liam Refsnes
Jenny Refsnes
Anja Refsnes
```

---

# Parâmetros x Argumentos

| Termo | Significado |
|---------|------------|
| Parâmetro | Variável declarada no método |
| Argumento | Valor enviado ao chamar o método |

Exemplo:

```java
static void myMethod(String nome)
```

- `nome` → parâmetro

```java
myMethod("Matheus");
```

- `"Matheus"` → argumento

---

# Múltiplos Parâmetros

Um método pode receber vários parâmetros.

```java
public class Main {

    static void myMethod(String fname, int age) {
        System.out.println(fname + " is " + age);
    }

    public static void main(String[] args) {

        myMethod("Liam", 5);
        myMethod("Jenny", 8);
        myMethod("Anja", 31);

    }

}
```

### Saída

```text
Liam is 5
Jenny is 8
Anja is 31
```

---

# Método com If/Else

Métodos podem conter estruturas condicionais normalmente.

## Exemplo

```java
public class Main {

    static void checkAge(int age) {

        if (age < 18) {
            System.out.println("Access denied - You are not old enough!");
        } else {
            System.out.println("Access granted - You are old enough!");
        }

    }

    public static void main(String[] args) {
        checkAge(20);
    }

}
```

### Saída

```text
Access granted - You are old enough!
```

---

# Métodos com Retorno

Quando queremos que um método devolva um valor, utilizamos um tipo de retorno em vez de `void`.

## Sintaxe

```java
static tipo nomeMetodo() {
    return valor;
}
```

---

# Retornando um Valor

```java
public class Main {

    static int myMethod(int x) {
        return 5 + x;
    }

    public static void main(String[] args) {

        System.out.println(myMethod(3));

    }

}
```

### Saída

```text
8
```

---

# Retornando a Soma de Dois Valores

```java
public class Main {

    static int myMethod(int x, int y) {
        return x + y;
    }

    public static void main(String[] args) {

        System.out.println(myMethod(5, 3));

    }

}
```

### Saída

```text
8
```

---

# Armazenando o Retorno em uma Variável

Esta é a forma mais recomendada.

```java
public class Main {

    static int myMethod(int x, int y) {
        return x + y;
    }

    public static void main(String[] args) {

        int z = myMethod(5, 3);

        System.out.println(z);

    }

}
```

### Saída

```text
8
```

---

# Void x Return

## Método sem retorno

```java
static void saudacao() {
    System.out.println("Olá!");
}
```

- Executa uma ação.
- Não devolve valor.

---

## Método com retorno

```java
static int soma(int a, int b) {
    return a + b;
}
```

- Executa uma ação.
- Devolve um valor.

---

# Boas Práticas

✅ Use nomes descritivos:

```java
calcularMedia()
validarSenha()
somarValores()
```

❌ Evite nomes genéricos:

```java
metodo1()
teste()
abc()
```

✅ Faça cada método realizar apenas uma responsabilidade.

✅ Reutilize métodos para evitar repetição de código.

---

# Resumo

| Conceito | Descrição |
|-----------|------------|
| Método | Bloco de código reutilizável |
| `void` | Não retorna valor |
| `return` | Retorna um valor |
| Parâmetro | Variável recebida pelo método |
| Argumento | Valor enviado ao método |
| `static` | Permite chamar o método sem criar objeto |
| Chamada de método | Executa o método |
| Método com retorno | Devolve um valor para quem o chamou |

---

# Sintaxes Mais Importantes para Decorar

### Método sem parâmetros

```java
static void saudacao() {
    System.out.println("Olá!");
}
```

### Método com parâmetros

```java
static void saudacao(String nome) {
    System.out.println(nome);
}
```

### Método com retorno

```java
static int soma(int a, int b) {
    return a + b;
}
```

### Chamando um método

```java
saudacao();
```

### Chamando com argumentos

```java
saudacao("Matheus");
```

### Recebendo retorno

```java
int resultado = soma(5, 3);
```
