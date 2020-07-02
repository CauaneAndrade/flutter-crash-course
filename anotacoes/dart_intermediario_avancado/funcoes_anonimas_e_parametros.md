Parâmetros opcionais


```dart
// parametros opcionais "{}" devem sempre ficam por último, a ordem importa
void exibirDados(String nome, {int idade, double altura}) {
    var novaAltura = altura ?? 0  // se altura for nula, novaAltura recebe 0
    print("nome: $nome");
    print("idade: $idade");
    print("altura: $novaAltura");
}

void calcularBonus() {
    print("Seu bônus é de: 50 reais");
}

// passar função como parâmetro "Function funcaoParametro"
void calcularSalario(double salario, Function funcaoParametro) {
    print("Seu salário é: $salario");
    funcaoParametro();  // executando a função recebida
}

void main() {
    exibirDados("Cauane", idade: 20, altura: 1.64);

    calcularSalario(1150, calcularBonus);
}
```

Função anônima

```dart
void calcularSalario(double salario, Function funcaoParametro) {
    print("Seu salário é: $salario");
    funcaoParametro();  // executando a função recebida
}

void main() {
    calcularSalario(1150, (){
        print("Seu bônus é de: 30 reais");
        }
    );  // função anônima
}
```