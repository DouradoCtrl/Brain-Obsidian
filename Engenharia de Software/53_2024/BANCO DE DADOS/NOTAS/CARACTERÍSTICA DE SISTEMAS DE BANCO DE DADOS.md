> SGBD => Mysql, PostgreSQL, Mysql e etc.
> é um software que permite criar, gerenciar e manipular bancos de dados.

**Algumas características:**
- **Natureza autodescritiva:** O banco de dados e as metainformações sobre os dados são armazenas conjuntamente. Essas informações contém o tipo, tamanho e restrições do banco de dados.

- **Isolamento entre programa e dados:** Com um SGBD, o programa só precisa saber que tipo de dados está guardando e não precisa se preocupar com a forma como esses dados são armazenados internamente. O SGBD cuida da organização e do acesso aos dados. Desse forma se torna mais fácil a manutenção e escalabilidade
 
- **Múltiplas visões dos dados:** Muitos SGBDs fornecem a possibilidade de que diferentes usuários com diferentes permissões possam acessar diferentes “visões” dos dados.

- **Acesso concorrente múltiplos usuários:** Permite que todos os usuários conectados executem operações ao mesmo tempo. Importante ressaltar que essa operações são feitas em fila, mas devido ao curto tempo dá a impressão de paralelismo.