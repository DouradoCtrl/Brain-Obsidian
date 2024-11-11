- Emite interrupção para a CPU para que um processo seja executado
	- Para que o processo seja executado sem qualquer interrupção
	- Desabilita a interrupção

**Funcionamentos**:
- Processo acessa sua R.C
- Interrupções desabilitadas
- Nenhum outro processo pode executar
- Processamento concluído
- Reabilitam-se interrupções

**Desvantagens:**
- Processo pode  "esquecer" de reabilitar
- Processo de usuário com mais prioridade que um processo de sistema
- Não funciona com múltiplas CPUs
	- Apenas a CPU do processo é afetada.