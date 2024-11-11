### Prevenção de Deadlocks

Para prevenir deadlocks, é necessário garantir que pelo menos uma das quatro condições para deadlock não ocorra. Aqui estão as estratégias para atacar cada condição:

1. **Exclusão Mútua**:
   - **Estratégia**: Alocar recursos somente se realmente necessário e limitar o número de processos que podem solicitar o recurso.
   - **Objetivo**: Reduzir a necessidade de exclusão mútua, por exemplo, usando recursos compartilháveis ou ajustando a alocação de recursos.

2. **Posse e Espera**:
   - **Estratégia**: Garantir que um processo, ao solicitar um recurso, não possua nenhum outro recurso. Ou, garantir que todos os recursos necessários estejam disponíveis antes da execução.
   - **Objetivo**: Evitar que um processo tenha que esperar enquanto segura outros recursos, evitando assim a posse e espera.

3. **Inexistência de Preempção**:
   - **Estratégia**: Implementar preempção, onde um recurso pode ser retirado de um processo e alocado a outro se necessário. 
   - **Objetivo**: Evitar que um recurso alocado não possa ser retirado e realocado quando um processo necessita de outros recursos.

4. **Espera Circular**:
   - **Estratégia**: Imposições de ordenação dos recursos. Cada processo deve requisitar recursos em uma ordem predefinida, evitando ciclos de espera circular.
   - **Objetivo**: Estabelecer uma ordem para a solicitação de recursos, garantindo que não haja encadeamento circular de processos esperando por recursos. 

Essas estratégias ajudam a criar um ambiente onde a probabilidade de deadlock é minimizada ou eliminada.