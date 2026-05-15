# SEMANA 1

### FUNDAMENTOS DO JAVA:
 - É uma linguagem tipada, ou seja, precisa informar o tipo de dados de todas as variáveis e métodos.

<hr>

# SEMANA 2

### ANOTAÇÕES:

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

Criar o método construtor, ou seja, um método que é chamado logo que a classe é instanciada:
```java
public class Exemplo {

 // Exemplo de método construtor, ele não possui o tipo de retorno e precisa ser exatamente o mesmo nome da classe.
 Exemplo() {
  System.out.println("Exemplo de um construtor.");
 }
}
```

Uso do this:
```java
String variavel;

this.variavel = "teste"; // atribui globalmente o valor para o atributo "variavel", exatamente como o "$this->" no PHP.
```

Solicitar ao usuário que informe alguma informação (como o input em python):
```java
import java.util.Scanner; // Primeiro precisa importar a classe do scanner.

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Depois cria o objeto e conecta o scanner à entrada do usuário (isto é, teclado, mouse, ou seja, coisas que a pessoa consegue interagir com o computador).
        System.out.print("Digite um número: ");
        int numero = scanner.nextInt(); // Depois atribui o valor à variável (isto para o programa e aguarda o usuário digitar, depois realiza a atribuição).

        if (numero > 0) {
            System.out.println("O número é positivo.");
        } else if (numero < 0) {
            System.out.println("O número é negativo.");
        } else {
            System.out.println("O número é zero.");
        }
   }
}

/*
Os mais utilizados tipos de scanners que capturam o que o usuário digita:
 - String Scanner.next(): retorna uma cadeia simples de caracteres, sem espaço. Em outras palavras, ele captura apenas a primeira palavra que você digitou.
 - String Scanner.nextLine(): retorna uma cadeia de caracteres, com espaço. Em outras palavras, ele captura tudo o que você digitou até apertar Enter, no teclado. Provavelmente este seria o “principal” substituto do input() do Python.
 - int Scanner.nextInt(): retorna um valor do tipo int.
double Scanner.nextDouble(): retorna um valor do tipo double, com ponto flutuante.

Atenção: se você usar nextInt() e logo em seguida nextLine(), o nextLine() vai ler o “Enter” que você apertou no seu teclado logo depois de ter digitado um número. Com isso, o nextLine() ficará vazio. Para resolver estes casos, crie um segundo nextLine(). Caso isso não tenha ficado claro, crie um pequeno código em Java para pedir um número inteiro (com nextInt) e depois um texto (com nextLine). Mostre o resultado dessas duas operações na tela. Depois faça o mesmo, agora com uma segunda chamada ao nextLine.
*/
```

Comparação de valores em Java:
```java
if (variavel1 == variavel2) { /* lógica */ } // é preferível NÃO utilizar este modelo.
if (Objects.equals(variavel1, variavel2)) { /* lógica */ } // mas sim este.
```

<hr>
