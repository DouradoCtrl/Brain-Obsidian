- Unidade da trabalho
- Realizada em qualquer sistema computacional
- O sistema precisa estar coerente antes e depois de sua execução
- Deve permitir que inúmeros cliente acessem sem que corrompa ou deixa incoerência

> **INSERT, UPDATE, DELETE, SELECT**
> Comando de transações em SQL
# ACID
---
**Propriedades:**
- **Atomicidade**
	- Indívisivel
	- Tudo ou nada
	- agrupar vários comandos relacionados com a garantia de que todos sejam executados
- **Consistência**
	- Mudança de Estados consistente após a transação
- **Isolamento**
	- Permite acesso múltiplo de usuários no SGDB
	- conjunto de transações terá o mesmo resultado de sua execução em série (uma após a outra
- **Durabilidade**
	- Garantia que após uma transação os dados sejam armazenados corretamente.
	- Mesmo com falhas, erros, pico de energia