```dart
void main() {
    // declarar variáveis
    // tipos: String, bool, int, double, dynamic

    // ao usar "var" não definimos tipo para a variável
    // é definido de acordo conteúdo
    var nome = "Cauane";
    const pi = 3.14;

    String cidade = "São José dos Campos";
    int idade = 20;
    double preco = 19.99;
    bool verdadeiroFalso = true;
    dynamic isVerdadeiroFalso = false;  // reconhece o tipo, lembra o "var"

    print("Meu nome é $nome");  // ou
    print("Meu nome é ${nome}");  // ou
    print("Meu nome é " + nome);

    /*
    Operadores lógicos
    - && → e
    - || → ou
    */
    bool resultado = true && true;

    /* 
    Controle de fluxo
    if → else → switch
    */
    var nota = 5;
    if (nota <= 5) {
        print("Reprovado");
    } else if (nota > 5 && nota <= 6 ) {
        print("Recuperação");
    } else {
        print("Aprovado");
    }

    // switch
    var comando = "depositar";
    switch(comando) {
        case "depositar":
            print("Deposite um valor");
            break;
        case "sacar":
            print("Saque um valor");
            break;
        default:
            print("Nenhuma opção escolhida, tente novamente");
    }

    /*
    Estrutura de repetição
    for → while
    */
    // while verifica antes de fazer a operação
    var numero = 0;
    while (numero <= 5) {
        print("Executando $numero");
        numero++;
    }

    // do while faz a operação e depois verifica
    numeroSegundo = 0;
    do {
        print("Executando $numero");
        numeroSegundo++;
    } while(numeroSegundo <= 5);

    for (int=1; i <=5; i++) {
        print("Executando $i");
    }
}
```