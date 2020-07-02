Construtor é um método especial para dar uma configuração inicial ao objeto

```dart
class User {
    String nameUser;
    String password;

    // contrutor
    // toda classe tem um construtor implícito
    // quando instanciamos uma classe, o construtor é chamado
    User(String user, String password) {
        // passamos para o contrutor apenas atributos que são essenciais para que o objeto esteja pronto p ser utilizado
        this.nameUser = user;
        this.password = password;
        print("configurações iniciais do objeto");
    }

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
    User user = new User("cauane", "123456");
    user.autenticar();
}
```

Outra forma de usar o construtor:

```dart
class User {
    String nameUser;
    String password;

    // contrutor
    // toda classe tem um construtor implícito
    // quando instanciamos uma classe, o construtor é chamado
    User(this.nameUser, this.password);

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
    User user = new User("cauane", "123456");
    user.autenticar();
}
```

Construtor nomeado (named constructor)

```dart
class User {
    String nameUser;
    String password;

    // contrutores
    // podemos ter mais de um construtor
    User(this.nameUser, this.password);
    User.director(this.nameUser, this.password) {
        // o nome do contrutor agora é "director"
        print("Libera provilégios");
    }

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
    // se quisermos chamar o construtor "director"
    User user = new User.director("cauane", "123456");

    // se não quisermos chamar o contrutor nomeado
    User user = new User("cauane", "123456");
}
```