# Orientação a Objetos

- Classe define como o objeto será, mas não é o objeto
- Objeto é elemento da vida real.
- Classe é o conceito, é a base, um modelo usado para construção do objeto
- Atributos definem as características do objeto
- Métodos são ações que podemos fazer com o objeto
- objeto é uma instância de uma classe

- métodos ficam dentro do escopo de uma classe, está associado a um objeto
- função 

```dart
// criar classes
class Casa {
    // atributos
    String cor;

    // métodos
    void abrirJanela() {
        print("Abrir janela da casa $cor");
    }

    void abrirCasa() {
        this.abrirJanela();
    }
}

void main() {
    // tipo - nome
    String nome = "Cauane";
    Casa minhaCasa = new Casa();  // "new" é opcional
    minhaCasa.cor = "Amarela";
    print(minhaCasa.cor);
}
```

Exercício

```dart
class User {
    String nameUser;
    String password;

    void autenticar() {
        var usuario = "cauane";
        var senha = "12345";

        if (this.nameUser == usuario && this.password == senha) {
            print("Usuário autenticado");
        } else {
            print("Usuário não autenticado");
        }
    }
}

void main() {
    User user = new User();
    user.nameUser = "cauane";
    user.password = "123456";
    user.autenticar();
}
```
