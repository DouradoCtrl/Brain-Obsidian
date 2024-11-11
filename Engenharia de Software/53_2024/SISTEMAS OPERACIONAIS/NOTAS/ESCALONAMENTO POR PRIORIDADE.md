> Baseado no Round-Robin: 

**Prioridades**
- Estabelecidas internamento pelo SO
- Alterada externamente (Usuário)
- Caso seja alta, maior acesso
- Windows: Task Manager
**Desvantagem**
- Caso o processo tenha uma prioridade elevada ele monopolisa o uso da CPU
- **Solução (Linux)**
	- Conforme o processo executar a prioridade vai caindo.
	- Se outro processo com prioridade maior aparecer há a troca da prioridade