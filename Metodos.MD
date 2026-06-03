# Métodos em Java

Os métodos são blocos de código reutilizáveis que executam uma tarefa específica.

Eles ajudam a organizar o programa, evitar repetição de código e facilitar a manutenção da aplicação.

> Em outras linguagens, métodos também são conhecidos como funções.

---

# Criando um Método

Um método deve ser declarado dentro de uma classe.

## Sintaxe

```java
public class Main {

    static void myMethod() {
        // código a ser executado
    }

}
```

### Componentes

| Elemento     | Descrição                                   |
| ------------ | ------------------------------------------- |
| `static`     | Permite chamar o método sem criar um objeto |
| `void`       | Indica que o método não retorna valor       |
| `myMethod()` | Nome do método                              |
| `{}`         | Bloco de código do método                   |

---

# Chamando um Método

Após criar um método, ele pode ser executado através de uma chamada.

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

# Parâmetros e Argumentos

Informações podem ser enviadas para um método através de parâmetros.

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

## Diferença

| Termo     | Significado                      |
| --------- | -------------------------------- |
| Parâmetro | Variável declarada no método     |
| Argumento | Valor enviado ao chamar o método |

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

# Métodos com If/Else

Métodos podem conter estruturas condicionais.

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

# Retorno de Valores

Quando desejamos que um método devolva um valor, utilizamos um tipo de retorno em vez de `void`.

## Exemplo

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

# Retornando Dois Parâmetros

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

# Armazenando o Retorno

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

# Sobrecarga de Métodos (Method Overloading)

A sobrecarga permite criar vários métodos com o mesmo nome, desde que possuam parâmetros diferentes.

## Exemplo

```java
int myMethod(int x)
float myMethod(float x)
double myMethod(double x, double y)
```

---

## Exemplo Prático

```java
public class Main {

    static int plusMethodInt(int x, int y) {
        return x + y;
    }

    static double plusMethodDouble(double x, double y) {
        return x + y;
    }

    public static void main(String[] args) {

        int myNum1 = plusMethodInt(8, 5);
        double myNum2 = plusMethodDouble(4.3, 6.26);

        System.out.println("int: " + myNum1);
        System.out.println("double: " + myNum2);

    }

}
```

### Saída

```text
int: 13
double: 10.56
```

---

# Escopo em Java

O escopo define onde uma variável pode ser acessada.

Uma variável só existe dentro da região onde foi criada.

---

# Escopo de Método

```java
public class Main {

    public static void main(String[] args) {

        int x = 100;

        System.out.println(x);

    }

}
```

A variável `x` só existe dentro do método `main()`.

---

# Escopo de Bloco

Variáveis criadas dentro de um bloco `{}` só podem ser utilizadas dentro dele.

```java
public class Main {

    public static void main(String[] args) {

        {

            int x = 100;

            System.out.println(x);

        }

    }

}
```

Fora do bloco, `x` não existe mais.

---

# Escopo de Loop

Variáveis declaradas dentro de um loop só existem durante a execução do loop.

```java
public class Main {

    public static void main(String[] args) {

        for (int i = 0; i < 5; i++) {
            System.out.println(i);
        }

    }

}
```

Após o término do loop, `i` não pode mais ser acessado.

---

# Recursão

Recursão é uma técnica onde um método chama a si mesmo.

Ela é útil para resolver problemas que podem ser divididos em versões menores do mesmo problema.

---

# Exemplo de Recursão

```java
public class Main {

    public static int sum(int k) {

        if (k > 0) {
            return k + sum(k - 1);
        } else {
            return 0;
        }

    }

    public static void main(String[] args) {

        int result = sum(10);

        System.out.println(result);

    }

}
```

### Saída

```text
55
```

---

# Condição de Parada

Todo método recursivo deve possuir uma condição de parada.

Sem ela, ocorrerá recursão infinita.

No exemplo anterior:

```java
if (k > 0)
```

Quando `k` chega a `0`, a recursão é encerrada.

---

# Recursão com Intervalo

```java
public class Main {

    public static int sum(int start, int end) {

        if (end > start) {
            return end + sum(start, end - 1);
        } else {
            return end;
        }

    }

    public static void main(String[] args) {

        int result = sum(5, 10);

        System.out.println(result);

    }

}
```

### Saída

```text
45
```

### Cálculo

```text
10 + 9 + 8 + 7 + 6 + 5 = 45
```

---

# Resumo

| Conceito           | Descrição                              |
| ------------------ | -------------------------------------- |
| Método             | Bloco de código reutilizável           |
| `void`             | Método sem retorno                     |
| `return`           | Retorna um valor                       |
| Parâmetro          | Variável recebida pelo método          |
| Argumento          | Valor enviado ao método                |
| Sobrecarga         | Mesmo método com parâmetros diferentes |
| Escopo             | Região onde uma variável existe        |
| Recursão           | Método chamando a si mesmo             |
| Condição de parada | Impede recursão infinita               |

---

# Sintaxes Mais Importantes

### Método simples

```java
static void saudacao() {
    System.out.println("Olá");
}
```

