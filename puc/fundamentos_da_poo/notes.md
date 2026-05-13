# SEMANA 1

### FUNDAMENTOS DO JAVA:
 - É uma linguagem tipada, ou seja, precisa informar o tipo de dados de todas as variáveis e métodos. 

Ponto de partida do código, para qualquer aplicação em Java funcionar precisa adicionar na linha onde o código se inicia:
```java
public static void main(String[] args) {
  // restante do código...
}
```

Síntaxe para fazer uma função:
```java
tipo_de_retorno nome_da_funcao(tipo_do_parametro parametro) {
// lógica da função...
}

// exemplo:
String informarNome(String nome) {
    System.out.printl("Seu nome é " + nome + "!");
}
```

Imprimir algo na tela:
```java
System.out.printl("Olá, mundo!");
```

Formatar string na hora de imprimi-la:
```java
String nome = "Lucas";
System.out.println("Olá, %s!", nome);

// Precisa passar como segundo parâmetro do print a variável que quer imprimir, e onde ela for ficar precisa informar de acordo com o seu tipo, como nos exemplos abaixo:
// %d -> um inteiro;
// %f -> um float;
// %s -> uma string.
```

Em Java qualquer número decimal é double por padrão, se quiser torná-lo float precisa declarar:
```java
float meuFloat = 10.5f; // obrigatório o 'f' ou 'F' no final;
double meuDouble = 10.5; // não precisa de sufixo.
```

<hr>
