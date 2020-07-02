No Dart não se tem herança múltipla

```dart
class Animal {
    String raca;

    void dormir() {
        print("Dormir");
    }
}

// herança "extends"
class Cachorro extends Animal{

}

void main() {
    Cachorro cachorro = new Cachorro();
    cachorro.raca = "Pitbull";
    print(cachorro.raca);
}

```