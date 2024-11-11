
Você foi contratado para desenvolver o sistema de gerenciamento de uma biblioteca. Sua tarefa é criar um banco de dados que permita armazenar e gerenciar informações sobre livros, autores, membros da biblioteca, empréstimos e categorias de livros. Após entrevistas com a empresa foram identificadas as seguintes informações:

**Identificação das Entidades e Atributos:**  
  
**Livro**: ISBN, título, ano de publicação.  
**Autor**: nome, nacionalidade.  
**Membro**: nome, e-mail, endereço (composto por CEP, rua, número e complemento), telefones (composto de número e tipo).  
**Empréstimo**: data_emprestimo, data_devolucao.  
**Categoria**: nome e descrição.  
**Editora**: nome, cidade, CNPJ.

**Relacionamentos:**  
  
• Um livro pode ter vários autores, e um autor pode escrever vários livros.  
• Um livro pode ser publicado por apenas uma editora, mas uma editora pode publicar vários livros.  
• Um livro pertence a uma categoria, e uma categoria pode incluir vários livros.  
• Um membro pode pegar emprestado vários livros, mas cada empréstimo é relacionado a apenas um membro.  
• Um empréstimo envolve um livro específico.  
**Considerações**: todas as entidades deverão possuir um atributo Identificador.  
   
**Para esta atividade mapa, você deve:**  
  
**1. Criar o Diagrama Entidade Relacionamento (DER)**, que representa o projeto conceitual, com o uso da notação de CHEN.  
**2. Criar o Modelo Entidade Relacionamento (MER)**, que representa o modelo lógico, por meio da tradução do DER criado anteriormente.  
**3. Criar o projeto físico, por meio de código SQL**, efetuando a criação do esquema de tabelas, respectivo ao MER criado anteriormente.  
   
**Como entregar a atividade:**  
  
A atividade deverá ser produzida em um arquivo do tipo TEXTO, conforme TEMPLATE anexado no MATERIAL DA DISCIPLINA, disponibilizado no Studeo, e DEVE ser entregue com a extensão (.PDF). Depois, deve ser anexado no ambiente da Atividade no STUDEO.  
   
**Dicas para realizar a atividade:**  
  
**1.** Durante as aulas, o professor fornecerá dicas que podem ser utilizadas para a confecção das suas atividades. Assim, é de suma importância participar das aulas ao vivo ou assisti-las posteriormente.  
**2.** Assista às aulas conceituais da disciplina.  
   
**Orientações:**  
• Plágios e cópias indevidas serão penalizados com descontos na nota, podendo chegar a zero.  
• Não são permitidas correções parciais no decorrer do módulo, pois a interpretação da atividade também faz parte da avaliação.  
• Atenção ao prazo de entrega da atividade. Sugerimos que envie sua atividade antes do prazo final para evitar transtornos e lentidão nos servidores. Evite o envio de atividade em cima do prazo.  
   
**Boa atividade!**

---

![[Pasted image 20240912172716.png]]

---

![[Pasted image 20240912172854.png]]

---
![[Pasted image 20240912172956.png]]