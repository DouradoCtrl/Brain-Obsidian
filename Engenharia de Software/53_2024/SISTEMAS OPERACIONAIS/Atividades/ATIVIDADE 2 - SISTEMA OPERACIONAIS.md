# 1)
Observe o diagrama esquemático de integração entre componentes em um sistema computacional:

![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222310_557840_1.png)

Fonte: o autor.
  
Há três papéis “humanos” apontados – usuário final, programador e projetista de sistema operacional. Todos eles são influenciados pelas decisões de projeto do sistema operacional, pois a depender de técnicas aplicadas no sistema operacional, a programação de utilitários e aplicativos será diferente. De mesma forma, o usuário terá uma percepção diferente do funcionamento geral, por direta influência das decisões de projeto.

Dado o contexto, qual é a influência da técnica de multiprogramação em um sistema operacional?

> Alternativas:

- A) Permite que vários programas sejam executados simultaneamente.
	- CERTA
- B) Garante a segurança do sistema contra ameaças.
	- ERRADA
- C) Aloca recursos de memória de forma eficiente.
	- ERRADA
- D) Aumenta a velocidade do processador.
	- ERRADA
- E) Automatiza tarefas repetitivas.
	- ERRADA
---
# 2)
Depois de criado, um [[Processo S.O|processo]] começa a executar e faz seu trabalho. Contudo, nada é para sempre, nem mesmo os processos. Mais cedo ou mais tarde o novo processo terminará,
normalmente em razão de alguma condições.  

Fonte: ​TANENBAUM, A. S. **Sistemas operacionais modernos.** 3. ed. São Paulo: Pearson Education, 2010.

Considerando o texto exposto, analise as alternativas a seguir sobre as descrições corretas para [[Término do processo S.O|encerramento de processos]], segundo Tanenbaum (2010): 

I. Término normal voluntário: ocorre quando o processo descobre a existência de um erro fatal, e com isto o estado de encerramento é acionado.  

II. Término por erro voluntário: ocorre quando o processo cumpre com êxito a sua finalidade ou então quando o usuário solicita voluntariamente o encerramento do processo.  

III. Erro fatal involuntário: ocorre durante a execução de um processo no momento que uma instrução ilegal ou não planejada/testada é executada.  

IV. Cancelamento por outro processo involuntário: ocorre quando um processo é finalizado a partir de um determinado programa que possui autoridade para realizar esta finalização, com privilégio superior (super usuário ou administrador).  
  
É correto o que se afirma em:

> Alternativas:

- A) I  e III, apenas.
	- ERRADA
- B) III e IV, apenas.
	- CORRETA
- C) I, III e IV, apenas.
	- ERRADA
- D) II, III, IV, apenas.
	- ERRADA
- E)  I, II, III, IV.
	- ERRADA
# 3)
No contexto de [[Concorrência de Processos e Condição de Corrida|concorrência entre processos]] e uso de recursos críticos, Tanenbaum (2010, p. 71) define "que uma boa solução de exclusão mútua deve atender a alguns critérios".  
 
​Fonte: TANENBAUM, A. S. **Sistemas operacionais modernos**. 3. ed. São Paulo: Pearson Education, 2010.

Considerando esta informação, analise os seguintes critérios:  
  
I. Dois processos nunca podem estar simultaneamente em suas regiões críticas.  
II. Nada pode ser afirmado sobre a velocidade ou sobre o número de CPUs.  
III. Nenhum processo executando fora de sua região crítica pode bloquear outros processos.  
IV. Nenhum processo deve esperar eternamente para entrar em sua região crítica.  
  
É correto o que se afirma em:

> Alternativas:

- (a) I e IV, apenas.
- (b) I, II e III, apenas.
- (c) I, III e IV, apenas.
- (d) II, III e IV, apenas.
- (e) I, II, III e IV.