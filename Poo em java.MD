[# Programação Orientada a Objetos (POO) em Java

## O que é POO?

Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o código em objetos.

Um objeto representa algo do mundo real, como:

- Pessoa
- Carro
- Conta Bancária
- Animal

A POO facilita a organização, reutilização e manutenção do código.

---

# Classe

Uma classe é um molde ou projeto para criar objetos.

Exemplo:

```java
public class Pessoa {

    String nome;
    int idade;

}
```

A classe Pessoa define que toda pessoa terá:

- nome
- idade

Porém, ainda não existe nenhuma pessoa criada na memória.

---

# Objeto

Um objeto é uma instância de uma classe.

Em outras palavras, é um elemento criado a partir do molde.

Exemplo:

```java
Pessoa p = new Pessoa();
```

Agora existe um objeto do tipo Pessoa.

Podemos atribuir valores aos seus atributos:

```java
p.nome = "Matheus";
p.idade = 19;
```

Visualmente:

Pessoa
├── nome = Matheus
└── idade = 19

Outro exemplo:

```java
Carro carro1 = new Carro();

carro1.marca = "Honda";
carro1.modelo = "Civic";
carro1.cor = "Preto";
```

---

# Atributos

Atributos são as características de um objeto.

Eles armazenam informações.

Exemplo:

```java
String marca;
String modelo;
int ano;
```

Nesse caso:

- marca → Honda
- modelo → Civic
- ano → 2025

Podemos pensar nos atributos como as informações que descrevem um objeto.

---

# Métodos

Métodos representam ações que um objeto pode realizar.

Enquanto os atributos descrevem o objeto, os métodos definem seus comportamentos.

Exemplo:

```java
public class Carro {

    String marca;
    String modelo;

    public void acelerar() {
        System.out.println("Acelerando...");
    }

}
```

O método acelerar() representa uma ação do carro.

Uso:

```java
Carro carro1 = new Carro();

carro1.acelerar();
```

Saída:

```

Acelerando...

```

---

# Construtor

O construtor é um método especial executado automaticamente quando um objeto é criado.

Sem construtor:

```java
Carro carro1 = new Carro();

carro1.marca = "Honda";
carro1.modelo = "Civic";
```

Precisamos atribuir os valores manualmente.

Com construtor:

```java
public class Carro {

    String marca;
    String modelo;

    public Carro(String marca, String modelo) {
        this.marca = marca;
        this.modelo = modelo;
    }

}
```

Agora podemos criar o objeto já preenchido:

```java
Carro carro1 = new Carro(
    "Honda",
    "Civic"
);
```

Isso torna o código mais organizado e seguro.

---

# Palavra-chave this

A palavra-chave this faz referência ao próprio objeto.

Exemplo:

```java
this.marca = marca;
```

Aqui existem duas variáveis chamadas marca:

```java
String marca;
```

Atributo da classe.

```java
String marca
```

Parâmetro recebido pelo construtor.

O Java precisa saber qual delas utilizar.

Por isso usamos:

```java
this.marca
```

que significa:

"Estou me referindo ao atributo da classe."

---

# Encapsulamento

Encapsulamento é o princípio de proteger os dados de um objeto.

A ideia é impedir alterações indevidas.

Exemplo:

```java
public class Conta {

    private double saldo;

}
```

A palavra:

```java
private
```

impede o acesso direto ao atributo.

Código inválido:

```java
conta.saldo = 1000;
```

O saldo fica protegido.

---

# Getter e Setter

Como o atributo é privado, precisamos criar métodos para acessá-lo.

## Setter

Responsável por modificar um valor.

```java
public void setSaldo(double saldo) {
    this.saldo = saldo;
}
```

## Getter

Responsável por retornar um valor.

```java
public double getSaldo() {
    return saldo;
}
```

Uso:

```java
Conta conta = new Conta();

conta.setSaldo(500);

System.out.println(conta.getSaldo());
```

Saída:

```

500.0

```

Benefício:

- Controle sobre os dados
- Maior segurança
- Melhor manutenção do sistema

---

# Herança

Herança permite reutilizar código.

Imagine:

- Cachorro
- Gato

Ambos possuem nome.

Sem herança:

```java
class Cachorro {
    String nome;
}
```

```java
class Gato {
    String nome;
}
```

O atributo nome fica repetido.

Com herança:

```java
public class Animal {

    String nome;

}
```

Classes filhas:

```java
public class Cachorro extends Animal {

}
```

```java
public class Gato extends Animal {

}
```

Estrutura:

Animal
│
├── Cachorro
│
└── Gato

Agora Cachorro e Gato herdam tudo que existe em Animal.

---

# Polimorfismo

Polimorfismo significa:

"Um mesmo método pode ter comportamentos diferentes."

Classe pai:

```java
public class Animal {

    public void emitirSom() {
        System.out.println("Som genérico");
    }

}
```

Classe filha:

```java
public class Cachorro extends Animal {

    @Override
    public void emitirSom() {
        System.out.println("Au Au");
    }

}
```

Outra classe filha:

```java
public class Gato extends Animal {

    @Override
    public void emitirSom() {
        System.out.println("Miau");
    }

}
```

Uso:

```java
Animal animal;

animal = new Cachorro();
animal.emitirSom();

animal = new Gato();
animal.emitirSom();
```

Saída:

```

Au Au
Miau

```

O mesmo método:

```java
emitirSom()
```

gera resultados diferentes dependendo do objeto.

---

# Os 4 Pilares da POO

## 1. Encapsulamento

Protege os dados.

Ferramenta principal:

```java
private
```

Exemplo:

```java
private double saldo;
```

---

## 2. Herança

Permite reutilizar código.

Ferramenta principal:

```java
extends
```

Exemplo:

```java
public class Cachorro extends Animal
```

---

## 3. Polimorfismo

Permite que um método tenha comportamentos diferentes.

Ferramenta principal:

```java
@Override
```

Exemplo:

```java
public void emitirSom()
```

---

## 4. Abstração

Consiste em mostrar apenas o necessário e esconder a complexidade.

Exemplo:

Ao dirigir um carro você utiliza:

- volante
- freio
- acelerador

Mas não precisa conhecer:

- pistões
- válvulas
- sistema de injeção

A complexidade fica escondida.

Esse é o conceito de abstração.

---

# Resumo Rápido para Prova

| Conceito | Definição |
|-----------|------------|
| Classe | Molde para criar objetos |
| Objeto | Instância criada a partir da classe |
| Atributo | Característica do objeto |
| Método | Ação do objeto |
| Construtor | Inicializa o objeto |
| this | Referência ao próprio objeto |
| Encapsulamento | Proteção dos dados |
| Getter | Obtém valores |
| Setter | Modifica valores |
| Herança | Reutilização de código |
| Polimorfismo | Mesmo método, comportamentos diferentes |
| Abstração | Esconder detalhes desnecessários |
