No desenvolvimento de software, a execução sequencial de instruções não é suficiente para criar programas dinâmicos e flexíveis que respondam a diferentes situações e condições. **Estruturas de controle** são fundamentais para determinar o fluxo de execução de um programa, permitindo que ele **tome decisões**, execute **certas ações repetidamente** ou escolha **entre diferentes caminhos de execução**.
 
Em Java, as estruturas de controle incluem instruções de sequência, seleção (como **if, else if, else, switch**) e repetição (como **while, do-while, for**). Essas estruturas são essenciais para implementar a **lógica condicional e de repetição**, que são comuns em algoritmos de resolução de problemas.
 
A partir dessa contextualização, **explique a importância das estruturas de controle em um programa Java.** Em sua resposta, **descreva os três tipos principais de estruturas de controle.**
  
ORIENTAÇÕES IMPORTANTES:
- Realize uma leitura cuidadosa do livro didático da disciplina e assista às aulas conceituais.
- Assista ao vídeo de orientações gravado pelo professor.
- Realize pesquisas complementares nas referências apresentada pelo professor.
- Ao realizar pesquisas, não faça cópia fiel do texto, e sempre insira as devidas referências dos autores.
 
Referências:
DEITEL, H. M. Java: como programar. 8. ed. [S. l.]: Prentice Hall Brasil, 2010.
HORSTMANN, C. S.; CORNELL, G. Core Java. Fundamentos. 8. ed. [S. l.]: Pearson, 2010. v. 1
HORSTMANN, C. S.; CORNELL, G. Core Java. Advanced Features. [S. l.]: Prentice Hall, 2008. v. 2.
SIERRA, K.; BATES, B. Use a cabeça! Java. 2. ed. [S. l.]: Alta Books, 2008.

# Resposta
---
[Livro Didático](POO-Unicesumar.pdf)
[Estruturas de Controle]()

 A estrutura de controle na aplicação é necessária para traçar a rota de instrução do algoritmo que você deseja para um usuário, com base nas informações que foram lidas pelo programa. Supondo que você deseja criar uma aplicação para validar se o menor tempo do corredor é maior que o tempo que foi lido posteriormente, você pode utilizar a estrutura de controle acompanhada de uma instrução para validar se o tempo é menor que o menor tempo armazenado na variável, dessa forma direcionando qual resposta será entregue para o usuário e como os dados lidos serão tratados com base na estrutura de controle aplicada.

Vale a pena ressaltar que nem todas as estruturas de controle são estruturas de repetição. Estruturas de controle como if, else if e switch são executadas somente uma vez na estrutura sequencial do programa. O mesmo executará aquele código somente se a condição da instrução for verdadeira; caso contrário, ele ignora aquela instrução aplicada no código da aplicação. Estruturas de repetição, por sua vez, controlam quantas vezes aquele código será executado ou até quando, fazendo um loop de repetição com base nas linhas de código dentro do seu escopo, sendo elas: for, while e do while. Segue abaixo um exemplo de algoritmo utilizando essas estruturas em Java.
 
 ```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = 0, i = 0;
        int menorTempo = 0;
        int corredor = 0;

        System.out.print("Digite o número de corredores: ");
        n = scanner.nextInt();
        int[] tempo = new int[n];

        for (i = 0; i < n; i++) {
            System.out.printf("Digite o tempo do %dº atleta: ", i + 1);
            tempo[i] = scanner.nextInt();

            if (i==0 || tempo[i] < menorTempo) {
                menorTempo = tempo[i];
                corredor = i + 1;
            }
        }

        System.out.printf("O recorde foi do %dº atleta foi de %d segundo(s)\n", corredor, menorTempo);
        
        scanner.close();
    }
}
```

Em minha utilização do dia a dia, eu utilizo 3 estruturas de controle principais para a construção de minhas aplicações, sendo elas: while, for e if/else if.

While: Executa o código enquanto a expressão for verdadeira. Somente quando a sua expressão é contrariada e retorna um valor booleano false, a estrutura de repetição é cessada. É interessante de ser utilizada quando não se tem certeza de quantas vezes o programa será repetido. Segue o exemplo abaixo:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean rep = true; 

        while(rep == true) {
            System.out.println("Você está dentro do loop while!");

            System.out.print("Deseja continuar? (s/n): ");
            String response = scanner.next();
            
            if (response.equalsIgnoreCase("n")) {
                rep = false;
            }
        }

        System.out.println("Au revoir");
        scanner.close();
    }
}
```

For: A expressão do seu código é subdividida no inicializador, delimitador (condição) e contador. Comumente é usado para controle de repetição quando se tem certeza de quantas vezes o código deverá ser repetido. Segue o exemplo abaixo:

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 0; i <= 5; i++) {
            System.out.printf("%d,", i);
        }
    }
}
```

If/else if: Estrutura de controle que direciona conforme os resultados de suas condições se os códigos dentro delas serão executados ou não, podendo, dessa forma, direcionar o caminho da lógica aplicada no algoritmo. Caso o retorno da condição seja true (verdadeiro), o código é executado; caso contrário, não é executado. Segue um exemplo abaixo:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite a sua idade: ");
        int idade = scanner.nextInt();

        if (idade < 0) {
            System.out.println("Idade inválida. Por gentileza, insira uma idade válida.");
        } else if (idade <= 12) {
            System.out.println("Você é uma criança.");
        } else if (idade <= 17) {
            System.out.println("Você é um adolescente.");
        } else if (idade <= 59) {
            System.out.println("Você é um adulto.");
        } else {
            System.out.println("Você é um idoso.");
        }

        scanner.close();
    }
}
``` 

# Referências
---
**NÚCLEO de Educação a Distância**; JUNIOR, Edson A. Oliveira; NOEL, Andre Abdala. *Programação Orientada a Objetos*. Florianópolis, SC: Arqué, 2023. Reimpressão em 2024. 176 p. ISBN 978-65-6083-308-1.


# Nota (opcional)
---
**Por gentileza, para melhor experiência na leitura da atividade, copie e cole o código em um leitor de texto que suporte formatação Markdown**


