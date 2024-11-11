1. [[PREVENÇÃO DE IMPASSES]]

**Impasse/Deadlock** é uma situação onde dois ou mais processos estão bloqueados, esperando um pelo outro para liberar recursos, resultando em uma condição onde nenhum processo pode avançar. Para que um impasse ocorra, quatro condições devem estar simultaneamente presentes:

1. **Exclusão Mútua:** Um recurso é usado por um processo de cada vez.
2. **Posse e Espera:** Um processo possui pelo menos um recurso e está esperando por outros recursos que estão sendo usados por outros processos.
3. **Inexistência de Preempção:** Recursos não podem ser retirados forçadamente de um processo; devem ser liberados voluntariamente.
4. **Espera Circular:** Há um ciclo de processos onde cada processo está esperando por um recurso que o próximo processo no ciclo está mantendo.

### Exemplo de Deadlock

1. **Processo A** está imprimindo um documento (usa **Impressora**).
2. **Processo B** está digitalizando um documento (usa **Scanner**).

**Passos do Deadlock:**

1. **Processo A** termina a impressão e precisa digitalizar um documento. Então, tenta usar o **Scanner**, mas o **Scanner** está sendo usado por **Processo B**.
2. **Processo B** termina a digitalização e precisa imprimir o documento. Então, tenta usar a **Impressora**, mas a **Impressora** está sendo usada por **Processo A**.

**Situação de Deadlock:**

- **Processo A** está bloqueado esperando o **Scanner**, que está sendo usado por **Processo B**.
- **Processo B** está bloqueado esperando a **Impressora**, que está sendo usada por **Processo A**.

Ambos os processos estão esperando um recurso que o outro processo possui, resultando em um impasse onde nenhum dos dois pode prosseguir.

# Questões Conceituais
#Sistemas_Operacionais/Conceitos 
O que é um deadlock e quais são as estratégias para preveni-lo?
??
Deadlock ocorre quando dois ou mais processos ficam bloqueados, esperando um pelo outro para liberar recursos. Para preveni-lo, pode-se:
1. **Evitar Exclusão Mútua**: Use recursos apenas se necessário e minimize o número de processos que podem requisitá-los.
2. **Evitar Posse e Espera**: Assegure que um processo não mantenha recursos enquanto espera por outros, ou garanta que todos os recursos necessários sejam alocados de uma vez.
3. **Evitar Inexistência de Preempção**: Permita a retirada de recursos de um processo se necessário para outros.
4. **Evitar Espera Circular**: Imponha uma ordem para requisitar recursos, evitando ciclos de espera.