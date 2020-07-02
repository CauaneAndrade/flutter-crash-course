Classes abstratas e concretas

concretas = conseguimos instanciá-la, conseguimos criar um objeto a partir da classe
abstratas: não conseguimos instanciá-la, não conseguimos criar um objeto a partir da classe

Em classes abstratas usa-se a keyword "abstract"
```dart
abstract class Animal {
    String cor;

    void correr();  // com o método sem corpo obrigamos as classes filhas a sobrescreverem o método correr
}

class Cao extends Animal {
    @override
    void correr() {
        print("Correr");
    }

    void latir() {
        print("Latir");
    }
}

class Gato extends Animal {
    @override
    void correr() {
        print("Correr");
    }

    void miar() {
        print("Miar");
    }
}

void main() {
    Cao cao = new Cao();
}
```