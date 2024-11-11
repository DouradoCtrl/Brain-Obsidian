> **Possibilita a utilização do armazenamento externo como extensão da memória RAM**

**Necessidade**
- Muitos processo precisam ser carregados por completo na memória para depois ser executado

**Swapping**
- Retira alguns processo da RAM para o disco rígido para liberar espaço para outro processo maior
- S.O atuais utilizam a memória virtual paginada
	- Transfere as páginas
	  
**Memória virtual paginadas algoritmo**
1. **First in First Out**
	- Páginas mais antigas retiradas primeiro
2. **Least Recently Used**
	- Menos recentemente usadas
3. **Not Recently Used**
	- Não usadas recentemente
---
#Sistemas_Operacionais/Conceitos 
Para que serve a memória virtual ?::A **memória virtual** utiliza armazenamento externo, como o disco rígido, como extensão da RAM para permitir a execução de mais processos e melhorar o desempenho.
