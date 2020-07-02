```dart

void main() {
    // Usando o Map podemos criar índices customizados
    // é como se fosse um dicionário: chave e valor
    Map frutas = Map();
    frutas["MO"] = "Morango";
    frutas["MA"] = "Manga";

    // chave e valor
    Map<int, String> estados = Map();
    estados[0] = "São Paulo";
    estados[1] = "Rio de Janeiro";
    estados[2] = "Minas Gerais";

    // métodos que temos a usar Maps
    print( estados.keys );
    print( estados.values );
    print( estados.containsKey(5) );
    print( estados.containsValue("São Paulo") );
    print( estados.length );

    // percorrer o Map
    estados.forEach(
        (chave, valor) => print("$chave - $valor")
    );

    // itens dinâmicos, sem tipo de valor especificado
    Map<String, dynamic> usuarios = Map();
    usuarios["nome"] = "Cauane";
    usuarios["idade"] = 20;
}
```