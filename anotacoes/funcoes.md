# estrutura

// tipo e nome do parâmetro
```dart
void exibirMensagem(String nome) {
    print("Hello, $nome!");
}

void calcularSalario(double salario) {
    var total = salario - 100;
    print("Salario total é: $total");
}

double funcaoRetorna(double numero) {
    var soma = numero + 2;
    return soma;
}

double testReturn(double numeroX) => numeroX * 2;

void main() {
    exibirMensagem("Cauane");
    calcularSalario(1150);
    print(funcaoRetorna(123));
    print(testReturn(5));
}
```