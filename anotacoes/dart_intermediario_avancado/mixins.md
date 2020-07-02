

```dart
abstract class Presidenciavel {
    void participarEleicao();
}

abstract class Cidadao {
    void direitosDeveres() {
        print("Nenhum direito, nenhum dever");
    }
}

mixin Escrita {
    void escreverArtigoJornal() {
        print("Escrever artigo para o jornal");
    }
}

class Obama extends Cidadao implements Presidenciavel {
    @override
    void participarEleicao() {
        print("Eleição americana");
    }
}

// para usar um "mixin" usamos a keyword "with"
class Cauane extends Cidadao with Escrita {

}
void main() {
    Obama obama = Obama();
    obama.direitosDeveres();
    obama.participarEleicao();
    
    Cauane cauane = Cauane();
    cauane.direitosDeveres();
    cauane.escreverArtigoJornal();
}
```