Servem para configurar um atributo que não queremos que seja acessado diretamente
Conseguimos fazer validações antes de configurar um valor

```dart
class Conta {
    double saldo = 0;
    double _saque = 0;  // siginifica que não devo acessar "saque" diretamente

    // Getter → obter
    double get saque {
        return this._saque;
    }
    // Setter → configurar
    set saque(double saque) {
        if (saque > 0 && saque <=500) {
            this._saque = saque
        }
    }
}

void main() {
    Conta conta = new Conta();
    conta.saque = 900;
    print(conta.saque);
}
```