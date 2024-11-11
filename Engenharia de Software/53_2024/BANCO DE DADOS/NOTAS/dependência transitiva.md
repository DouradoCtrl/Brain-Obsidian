## O que é ?
> Em normalização de banco de dados, uma **dependência transitiva** ocorre quando um atributo não-chave é dependente de outro atributo não-chave, que por sua vez depende da chave primária da tabela.

## Como eliminar ?
> Para eliminar a dependência transitiva, você precisa **remover o atributo dependente da tabela original** e **criá-lo em uma nova tabela**, onde ele dependerá diretamente da chave primária dessa nova tabela.
