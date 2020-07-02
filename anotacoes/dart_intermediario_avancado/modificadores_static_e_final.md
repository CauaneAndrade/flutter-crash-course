Forma padrão de acessar atributos da classe
```dart
class Configuracao {
    String idApp = "HASH12345";
    String notificacaoSom = "sim";
}

void main() {
    // para acessar "idApp" e "notificacaoSom" preciso instanciar a classe "Configuracao"
    Configuracao config = Configuracao();
    print(config.idApp);
}
```

Se não quisermos instanciar a classe para acessar o atributo "idApp",
podemos usar o modificador de acesso "static"
usamos para definir um valor constante

| ao definir atributos e/ou métodos estáticos a classe consome mais recursos do que uma classe que instânciamos
```dart
class Configuracao {
    static String idApp = "HASH12345";
    static String notificacaoSom = "sim";

    // o modificador "static" pode ser usado em métodos também
    static void configuracaoInicial() {
        print("Executa configurações iniciais");
    }
}

void main() {
    print(Configuracao.idApp);
    print(Configuracao.notificacaoSom);
    Configuracao.configuracaoInicial();
}
```

Modificador "final"
```dart
class Conta {
    double valor;
}

void main() {
    final Conta conta = Conta();
    // ao usar o final declaramos que este é o objeto final e não pode ser alterado
    // Once assigned a value, a final variable's value cannot be changed.
    conta.valor = 115.0;
    print(conta.valor);
}
```