> Controle de acesso de uma região crítica a partir de uma variável binária

- Processo solicita o uso da região crítica, se estiver vazia valor 0
- Se estiver em uso, valor 1

**Desvantagem:**
- Lock é um recurso compartilhado;
- Acesso simultâneo à R.C
	1. Um processo tem permissão concedida;
	2. Um segundo processo pede acesso;
	3. O primeiro ainda não mudo de 0 p/ 1
		- logo, dois processo na R.C