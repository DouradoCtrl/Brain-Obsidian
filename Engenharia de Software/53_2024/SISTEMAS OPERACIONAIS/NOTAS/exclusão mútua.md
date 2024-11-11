### O que é Exclusão Mútua?
**Exclusão mútua** significa garantir que apenas uma thread ou processo possa acessar a região crítica de cada vez. Isso evita que duas ou mais threads ou processos interfiram entre si ao tentar modificar um recurso compartilhado simultaneamente.

### Como Funciona?
Quando uma thread quer entrar na região crítica, ela precisa primeiro "trancar a porta" usando um mecanismo de exclusão mútua, como uma **trava (lock)**. Enquanto a thread está na região crítica, outras threads são bloqueadas de entrar até que a primeira termine e "destranque a porta", liberando o recurso para a próxima thread.

### Por que é Importante?
A exclusão mútua é fundamental para evitar erros como condições de corrida, onde o resultado do programa depende da ordem imprevisível de execução das threads. Ao garantir que apenas uma thread possa acessar a região crítica por vez, a exclusão mútua mantém a integridade dos dados e o comportamento correto do programa.
### Critérios exclusão mútua:
Segundo Tanenbaum (2010) a exclusão mútua eficiente devem respeitar o seguintes parâmetros.

- Dois processos nunca podem estar  simultaneamente em suas regiões críticas.
- Nada pode ser afirmado sobre a velocidade ou sobre o número de CPUs.
- Nenhum processo executando fora de sua região crítica pode bloquear outros processos.
- Nenhum processo deve esperar eternamente para entrar em sua região crítica.
