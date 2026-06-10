 Orientação a Objetos

Criando uma classe:

public class Pessoa {

    String nome;
    int idade;

}

Criando objeto:
Objeto é algo criado a partir da classe.
Pessoa p = new Pessoa();

p.nome = "Matheus";
p.idade = 19;

Carro carro1 = new Carro();

carro1.marca = "Honda";
carro1.modelo = "Civic";
carro1.cor = "Preto";

Atributos
Atributos são as características do objeto.

String marca;
String modelo;
int ano;


Métodos
Métodos são ações

public class Carro {

    String marca;
    String modelo;

    public void acelerar() {
        System.out.println("Acelerando...");
    }

}

uso

Carro carro1 = new Carro();

carro1.acelerar();


Construtor


Ao invés de Carro carro1 = new Carro();

carro1.marca = "Honda";
carro1.modelo = "Civic";


Use um construtor 

public class Carro {

    String marca;
    String modelo;

    public Carro(String marca, String modelo) {
        this.marca = marca;
        this.modelo = modelo;
    }


Criando objeto:

Carro carro1 = new Carro(
    "Honda",
    "Civic"
);

O que é this?

this.marca = marca;

O Java fica confuso porque existem duas variáveis chamadas marca.


Encapsulamento

Encapsulamento serve para proteger os dados
usando privatee
Exemplo:

public class Conta {

    private double saldo;

}


Agora ninguém pode alterar diretamente.

Getter e Setter

Para controlar o acesso.

Setter:

public void setSaldo(double saldo) {
    this.saldo = saldo;
}

Getter:
public double getSaldo() {
    return saldo;
}

Conta conta = new Conta();

conta.setSaldo(500);

System.out.println(conta.getSaldo());

Herança


Imagine:

Temos:

Cachorro
Gato

Ambos são animais.


Sem herança:
class Cachorro {
    String nome;
}
class Gato {
    String nome;
}

Código repetido.

Com herança:
public class Animal {

    String nome;

}


public class Cachorro extends Animal {

}

public class Gato extends Animal {

}

resultado

Animal
│
├── Cachorro
│
└── Gato


Polimorfismo

O mesmo método pode ter comportamentos diferentes.

Classe pai:
public class Animal {

    public void emitirSom() {
        System.out.println("Som genérico");
    }

}


Classe filha:
public class Cachorro extends Animal {

    @Override
    public void emitirSom() {
        System.out.println("Au Au");
    }

}


Animal animal;

animal = new Cachorro();
animal.emitirSom();

animal = new Gato();
animal.emitirSom();


Os 4 pilares da POO

1. Encapsulamento

Protege os dados.

private

2. Herança

Reaproveita código.

extends


3. Polimorfismo

@Override
