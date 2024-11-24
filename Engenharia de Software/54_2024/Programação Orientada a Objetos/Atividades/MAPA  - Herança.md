# Descrição
---
Estudante,

Temos por certo que os desafios sempre contribuem com a aquisição de conhecimentos e competências desejadas. Assim, faz-se necessário relacionar o que se aprende com situações reais que podem ser encontradas no cotidiano. Você é convidado a realizar uma atividade discursiva para verificar como a disciplina em questão pode contribuir para a sua experiência e formação profissional.   
  
​No desenvolvimento de software orientado a objetos, conceitos como herança e polimorfismo são fundamentais para a criação de sistemas flexíveis, reutilizáveis e extensíveis. A linguagem Java, com seu suporte robusto a esses conceitos, permite que os desenvolvedores implementem soluções que aproveitam ao máximo a modularidade e a reutilização de código.  
  
Herança permite que uma classe derive características de outra, promovendo a reutilização de código e a criação de hierarquias de classes. Polimorfismo, por outro lado, permite que objetos de diferentes classes sejam tratados como objetos de uma classe comum, facilitando o uso de uma interface comum para diferentes tipos de objetos.  
   
Com base nessa breve contextualização e no estudo da disciplina:  
a) Explique o conceito de herança em Java e explique como ela pode ser utilizada para promover a reutilização de código. Dê um exemplo de como uma classe base e uma classe derivada podem ser implementadas em Java.  
  
b) Defina polimorfismo e descreva como ele pode ser utilizado em Java para permitir a utilização de métodos de forma dinâmica. Forneça um exemplo de código em Java que demonstre o uso de polimorfismo.  
   
**ORIENTAÇÕES IMPORTANTES:**  
- Lembre-se que a interpretação da atividade também faz parte da avaliação.  
- Acesse o link com o vídeo gravado pelo professor para ajudá-lo na realização desta atividade MAPA. O acesso deverá ser realizado em: Materiais >> Material da Disciplina.  
- Realize pesquisas complementares nas referências apresentadas pelo professor.  
- Ao realizar pesquisas, não faça cópia fiel do texto e sempre insira as devidas referências dos autores.  
- A entrega deve ser feita exclusivamente por meio do _Template_ de entrega da atividade MAPA disponível no Material da Disciplina.  
- Antes de enviar sua atividade, certifique-se de que respondeu a todas as perguntas e realize uma cuidadosa correção ortográfica.  
- Após o envio não são permitas alterações, ou modificações. Logo, você tem apenas uma chance de enviar o arquivo corretamente. Revise bem antes de enviar!​  
- Procure sanar suas dúvidas junto à mediação em tempo hábil sobre o conteúdo exigido na atividade, de modo que consiga realizar sua participação.  
- Atenção ao prazo de entrega, evite envio de atividade em cima do prazo. Você pode ter algum problema com internet, computador, software etc., e os prazos não serão flexibilizados, mesmo em caso de comprovação.  
  
Em caso de dúvidas, encaminhar mensagem ao seu Professor Mediador.  
Bons estudos!  
​  
**Referências**:  
DEITEL, H. M. **Java**: como programar. 8. ed. [_S. l._]: Prentice Hall Brasil, 2010.  
HORSTMANN, C. S.; CORNELL, G. **Core Java**. v. 1. Fundamentos. 8. ed. [_S. l._]: Pearson, 2010.  
HORSTMANN, C. S.; CORNELL, G. **Core Java**. v. 2. Advanced Features. [_S. l._]: Prentice Hall, 2008.  
SIERRA, K.; BATES, B. **Use a cabeça**! Java. 2. ed. [_S. l._]: Alta Books, 2008.

# Resposta
---
- herança e polimorfismo

O que eu quero fazer.
	-> Uma atividade básica utilizando um classe abstrata que vai funcionar como um super classe para as outras classes.
	-> Quero fazer uma classe abstrata com pessoa e as demais classes vai ser estudante e professor, ambos terão um apresentar porém o polimorfismo fará com que cada apresentação de cada um seja diferente, e o método abstrato irá definir um padrão de classes que irão derivar da mesma.
	
**O que é herança e polimorfismo ?**
livro e fontes externas
**Como pode ser usado em java ?**
exemplo analise
	- sem abstracao
	- com abstracao
**Qual sua importância ?**
reutilizacao de codigo, padronizacao

### Exemplo 1 (Herança, Polimorfismo)
- Classe Main
```java
package mapaUnicesumar.herance;  
  
public class Main {  
    public static void main(String[] args) {  
        Pessoa Sabrina = new Pessoa("Sabrina", "324.324.234-54", 21);  
  
        Dicente Samuel = new Dicente("Samuel", 20, "026.143.324-54", "24039423-5",  
               "Engenharia de Software", "Programação Orientada a Objetos");  
  
        Samuel.apresentar();  
  
        Docente Emmanuel = new Docente("Emmanuel", 35, "432.342.123-43",  
               "Redes de Computadores", "Unicesumar");  
  
        Emmanuel.apresentar();  
        }  
}
```

- Superclasse
```java
package mapaUnicesumar.herance;  
  
public class Pessoa {  
    private String nome;  
    private String cpf;  
    private Integer idade;  
  
    public Pessoa(String nome, String cpf, Integer idade) {  
        this.setNome(nome);  
        this.setCpf(cpf);  
        this.setIdade(idade);  
    }  
    public String getCpf() {  
        return cpf;  
    }  
  
    public void setCpf(String cpf) {  
        this.cpf = cpf;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public Integer getIdade() {  
        return idade;  
    }  
  
    public void setIdade(Integer idade) {  
        this.idade = idade;  
    }  
  
  
    public void apresentar() {  
        System.out.println("Olá, meu nome é " + nome);  
    }  
      
}
``` 

- Subclasse Docente
```java
package mapaUnicesumar.herance;  
  
public class Docente extends Pessoa {  
    private String disciplina;  
    private String instituicao;  
  
    public Docente(String nome, Integer idade, String cpf, String disciplina, String instituicao) {  
        super(nome, cpf, idade);  
        this.disciplina = disciplina;  
        this.instituicao = instituicao;  
    }  
  
    @Override  
    public void apresentar() {  
        System.out.printf("O meu nome é %s e sou professor de %s na instituição de ensino %s",  
            getNome(), disciplina, instituicao);  
    }  
}
```

- Subclasse Dicente
```java
package mapaUnicesumar.herance;

public class Dicente extends Pessoa {
    private String matricula;
    private String curso;
    private String disciplina;
    
    public Dicente(String nome, Integer idade, String cpf, String matricula, String curso, String disciplina) {
        super(nome, cpf, idade);
        this.matricula = matricula;
        this.curso = curso;
        this.disciplina = disciplina;
    }
}

```

- Saída compilado
...
#### Análise:

### Exemplo 1 (Abstração, Herança, Polimorfismo)
- Classe Main
```java
package novoExemplo;

public class Main {
    public static void main(String[] args) {
        Estudante Samuel = new Estudante("Samuel", 20);
        Samuel.apresentar();

        Professor Glauber = new Professor("Glaube");
        Glauber.apresentar();

    }
}

```

- Superclasse
```java
package novoExemplo;  
  
public abstract class Pessoa {  
    private String nome;  
    private String cpf;  
    private Integer idade;  
  
    public abstract void apresentar();  
  
    public String getCpf() {  
        return cpf;  
    }  
  
    public void setCpf(String cpf) {  
        this.cpf = cpf;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public Integer getIdade() {  
        return idade;  
    }  
  
    public void setIdade(Integer idade) {  
        this.idade = idade;  
    }  
  
}
```

- Classe filha Estudante
```java
package novoExemplo;

public class Estudante extends Pessoa {;

    public Estudante(String nome, Integer idade) {
        this.setNome(nome);
        this.setIdade(idade);
    }

    @Override
    public void apresentar() {
        System.out.printf("Olá, me chamo %s tenho %d anos e atualmente sou estudante",
                getNome(), getIdade());
    }
}
```

- Classe filha Professor
```java
package novoExemplo;

public class Professor extends Pessoa{

    public Professor(String nome) {
        this.setNome(nome);
    }


    @Override
    public void apresentar() {
        System.out.printf("Olá, meu nome é %s e eu sou o professor dessa disciplina", getNome());
    }
}

```

- Saída compilado
...

#### Análise:


## **Referências**
---
