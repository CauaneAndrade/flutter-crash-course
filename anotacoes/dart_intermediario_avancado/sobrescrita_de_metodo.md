```dart
class Animal {
    String raca;

    void dormir() {
        print("Dormir");
    }

    void correr() {
        print("Correr");
    }
}

// herança "extends"
class Cachorro extends Animal {
    @override  // sobrepor
    void correr() {
        print("Correr como um cachorro");
    }
}
class Gato extends Animal {
    @override  // sobrepor
    void correr() {
        print("Correr como um gato");
    }
}

void main() {
    Cachorro cachorro = new Cachorro();
    Gato gato = new Gato();
    cachorro.correr();
    gato.correr();
}
```

Sobrepor parcialmente
```dart
class Animal {
    String raca;

    void dormir() {
        print("Dormir");
    }

    void correr() {
        print("Correr como um");
    }
}

// herança "extends"
class Cachorro extends Animal {
    @override  // sobrepor
    void correr() {
        super.correr();
        print("cachorro");
    }
}
class Gato extends Animal {
    @override  // sobrepor
    void correr() {
        super.correr();
        print("gato");
    }
}

void main() {
    Cachorro cachorro = new Cachorro();
    Gato gato = new Gato();
    cachorro.correr();
    gato.correr();
}
```

Sobrepor Construtor
```dart
class Animal {
    String raca;

    Animal(this.raca);

    void dormir() {
        print("Dormir");
    }

    void correr() {
        print("Correr como um");
    }
}

// herança "extends"
class Cachorro extends Animal {
    // sobrepor construtor
    // Cachorro(this.raca);  // não posso fazer isso, pois a classe ainda não está instanciada
    Cachorro(String raca) : super(raca);

    @override  // sobrepor
    void correr() {
        super.correr();
        print("cachorro");
    }
}

void main() {
    Cachorro cachorro = new Cachorro("Pitbull");
    print("Raça do cachorro: ${cachorro.raca}");
}
```