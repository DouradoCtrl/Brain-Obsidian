**Bibliotecário Chefe**  
   
Como bibliotecário chefe de uma grande biblioteca pública, tenho a visão de modernizar nossos serviços de empréstimo de livros e acesso a recursos educacionais. A biblioteca tem um vasto acervo de livros, revistas, e materiais multimídia que atualmente são gerenciados manualmente ou através de um sistema local defasado. Nosso objetivo é criar um Sistema de Biblioteca Online que possa ser acessado por nossos usuários de qualquer lugar, facilitando o acesso ao acervo, aos serviços de empréstimo e à administração de contas de usuário. Este sistema deve não apenas atender às necessidades atuais, mas também ser escalável para suportar futuras expansões e integrações.  
   
Necessidades do Sistema  
1. Acesso Remoto: Usuários devem poder acessar o sistema de qualquer lugar, utilizando dispositivos como computadores, tablets e smartphones.  
2. Catálogo de Acervo: O sistema deve permitir a navegação, busca e visualização detalhada dos itens do acervo da biblioteca.  
3. Gerenciamento de Empréstimos: Usuários devem poder reservar e renovar empréstimos de livros online.  
4. Conta de Usuário: Cada usuário deve ter uma conta pessoal onde possa visualizar seu histórico de empréstimos, multas, e reservas.  
5. Administração do Sistema: Bibliotecários devem poder adicionar, remover e atualizar itens no acervo, gerenciar contas de usuários e monitorar empréstimos.  
   
Requisitos Funcionais  
1. RF001 - Cadastro de Usuários  
   - O sistema deve permitir que novos usuários se registrem criando uma conta com informações pessoais básicas.  
2. RF002 - Autenticação de Usuários  
   - O sistema deve fornecer opções de login para que os usuários possam acessar suas contas.  
3. RF003 - Catálogo de Livros  
   - O sistema deve permitir que os usuários pesquisem livros por título, autor, gênero, ou ISBN.  
4. RF004 - Visualização de Detalhes do Livro  
   - O sistema deve exibir informações detalhadas sobre um livro, como título, autor, sinopse, número de páginas, e disponibilidade.  
5. RF005 - Empréstimo de Livros  
   - O sistema deve permitir que os usuários reservem livros para empréstimo, especificando a data de retirada.  
6. RF006 - Renovação de Empréstimos  
   - O sistema deve permitir que os usuários renovem seus empréstimos, se o livro não estiver reservado por outro usuário.  
7. RF007 - Histórico de Empréstimos  
   - O sistema deve fornecer um histórico de todos os empréstimos feitos por um usuário.  
8. RF008 - Gestão de Multas  
   - O sistema deve calcular e exibir multas por atraso de devolução de livros.  
9. RF009 - Adição e Atualização de Livros (Admin)  
   - Bibliotecários devem poder adicionar novos livros ao catálogo, bem como atualizar ou remover livros existentes.  
10. RF010 - Gerenciamento de Contas de Usuário (Admin)  
    - Bibliotecários devem poder visualizar, suspender e excluir contas de usuários.  
   
Descrição dos Fluxos do Caso de Uso  
   
1. Cadastro de Usuários  
**Ator**: Novo Usuário  
1. O novo usuário acessa a página de cadastro.  
2. O usuário preenche suas informações pessoais (nome, email, senha). 
3. O sistema valida as informações e cria uma nova conta de usuário.  
4. O usuário recebe uma confirmação do cadastro via email.  
   
2. Empréstimo de Livros  
**Ator**: Usuário Registrado  
1. O usuário faz login no sistema.  
2. O usuário navega ou busca o catálogo de livros.  
3. O usuário seleciona um livro e solicita o empréstimo.  
4. O sistema verifica a disponibilidade do livro.  
5. O sistema registra o empréstimo e atualiza o status do livro.  
6. O usuário recebe uma confirmação do empréstimo e a data de devolução.  
   
3. Adição de Livros (Admin)  
**Ator**: Bibliotecário  
1. O bibliotecário faz login no sistema com permissões administrativas.  
2. O bibliotecário acessa a seção de gerenciamento de livros.  
3. O bibliotecário preenche as informações do novo livro (ISBN, título, autor, etc.).  
4. O sistema valida as informações e adiciona o novo livro ao catálogo.  
5. O bibliotecário recebe uma confirmação da adição do livro.  
   
Para esta atividade de mapa, crie um diagrama de classe considerando as seguintes classes: Usuario, Bibliotecario, Livro, Emprestimo e Biblioteca.  
  
**​IMPORTANTE:**  
1. Acesse o link com um vídeo tutorial para ajudá-lo nesse processo de criação e desenvolvimento. O acesso deverá ser realizado em: Materiais >> Material da Disciplina ou no Fórum Interativo.  
2. Responda a todos os itens, seguindo como roteiro os tópicos elencados anteriormente, e coloque em um único arquivo.  
3. A entrega deve ser feita por meio do Template de entrega da atividade MAPA, disponível no material da disciplina.  
4. Antes de enviar sua atividade, certifique-se de que respondeu a todas as perguntas e realize uma cuidadosa correção ortográfica.  
5. Após o envio não são permitas alterações, ou modificações. Logo, você tem apenas uma chance de enviar o arquivo corretamente. Revise bem antes de enviar!  
6. Lembre-se de que evidências de cópias de materiais, incluindo de outros estudantes, sem devidas referências, serão inquestionavelmente zeradas. As citações e referências, mesmo que do livro da disciplina, devem ser realizadas conforme normas da Instituição de Ensino.  
7. Não são permitidas correções parciais no decorrer do módulo, ou seja, o famoso: “professor, veja se minha atividade está certa?”. Isso invalida seu processo avaliativo. Lembre-se de que a interpretação da atividade também faz parte da avaliação.  
8. Procure sanar suas dúvidas junto à mediação em tempo hábil sobre o conteúdo exigido na atividade, de modo que consiga realizar sua participação.  
9. Atenção ao prazo de entrega, evite envio de atividade em cima do prazo. Você pode ter algum problema com internet, computador, software etc., e os prazos não serão flexibilizados, mesmo em caso de comprovação.  
10. Para realização da atividade você poderá utilziar o aplicativo de sua preferência.   
  
Bons estudos!  
Em caso de dúvidas, encaminhar mensagem pelo Fale com o Mediador!

CLASSES:
	USUARIO
	EMPRESTIMO
	LIVROS
	BIBLIOTECARIO

### Diagrama de Classes

1. **Classe Usuario**
    
    - **Atributos:**
        - id: int
        - nome: string
        - email: string
        - senha: string
        - historicoEmprestimos: List<Emprestimo>
    - **Métodos:**
        - cadastrar()
        - autenticar()
        - visualizarHistorico()
2. **Classe Bibliotecario (herda de Usuario)**
    
    - **Atributos:**
        - idBibliotecario: int
    - **Métodos:**
        - adicionarLivro()
        - atualizarLivro()
        - gerenciarContas()
3. **Classe Livro**
    
    - **Atributos:**
        - id: int
        - titulo: string
        - autor: string
        - isbn: string
        - sinopse: string
        - numeroPaginas: int
        - disponivel: boolean
    - **Métodos:**
        - atualizarDisponibilidade()
        - exibirDetalhes()
4. **Classe Emprestimo**
    
    - **Atributos:**
        - id: int
        - livro: Livro
        - usuario: Usuario
        - dataEmprestimo: Date
        - dataDevolucao: Date
        - status: string (ativo, finalizado)
    - **Métodos:**
        - renovar()
        - calcularMulta()
5. **Classe Biblioteca**
    
    - **Atributos:**
        - nome: string
        - endereco: string
        - acervo: List<Livro>
    - **Métodos:**
        - buscarLivro()
        - visualizarCatalogo()