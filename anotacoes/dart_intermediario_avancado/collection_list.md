São estruturas de dados usadas para armazenar ítens

Temos dois tipos de Collection com o Dart:
- List
- Maps

```dart

void main() {
    // podemos criar listas desta forma
    var lista = ["Morango", "Abacate"];

    // usando a Collection List, usamos desta forma
    List<String> frutas = ["Pêra", "Goiaba"];
    List<int> numeros = [1, 2, 3];

    // Podemos criar uma lista sem tipo definido
    // pode-se adicionar na lista elementos de vários tipos
    List random = ["Cauane", 5.6, 10];

    // Alguns métodos que temos ao usar List
    frutas.add("Melância");
    frutas.insert(0, "Banana");  // adicionar um item na posição especificada
}
```