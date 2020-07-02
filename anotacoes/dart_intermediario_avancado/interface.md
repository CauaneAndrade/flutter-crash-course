Interface é um contrato que quando assumido por uma classe deve ser implementado

Podemos ter mais de uma Interface

```dart
abstract class Presidenciavel {
    void participarEleicao();
}

abstract class Cidadao {
    void direitosDeveres() {
        print("Nenhum direito, nenhum dever");
    }
}
class Obama extends Cidadao implements Presidenciavel {
    @override
    void participarEleicao() {
        print("Eleição americana");
    }
}

class Cauane extends Cidadao {

}
void main() {
    Obama obama = Obama();
    obama.direitosDeveres();
    obama.participarEleicao();
    
    Cauane cauane = Cauane();
    cauane.direitosDeveres();
}
```