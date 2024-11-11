Por favor, gostaria que você me informasse todas as ações realizadas nos meses de julho e agosto. Além disso, peço que verifique se todas as demandas planejadas para esse período foram devidamente concluídas. Também seria importante que você descrevesse como é sua rotina diária.

Peço que todas essas informações sejam organizadas em um documento e encaminhadas até, no máximo, amanhã, 03/09/2024

---
Minha promoção veio no dia 24 de agosto de 2024, e este relatório apresenta meus resultados e atividades realizadas no dia a dia como NOC. 

No dia-a-dia no final do mês de julho a  31 de agosto, minhas atividades em expediente foram voltadas a Telefonia Fusion, Anlix, Monitoramentos de incidentes, monitoramentos dos links de conexão, monitoramento analíticos de serviço de mitigação Wanguard, documentação de processos, desenvolvimento do fidelize. .

Dia 24 julho até dia 30 de agosto:
# Telefonia
Dentre as atividades de telefonia do dia 24 à 31 de agosto foi necessário alinhar a planilha, pois havia alguns clientes que já estavam cancelados mas ainda estavam com o número disponível no fusion.

Além de portabilidades e uma reversão de cancelamento de telefonia da cliente Jaqueline, uma vez que os nossos números de telefonia não recebia ligação a cobrar, foi preciso abrir um chamado com a NWI para rever essa questão. 

O conhecimento de telefonia foi expandido para além do fusion, passei a utilizar outras ferramentas como MobXTerm utilizando SNGREP, MICROSIP para testes de entrante e sainte de ligação e WireShark. 

A partir do dia 15 de agosto até o dia 30, fiquei encarregado 100% pela telefonia devidos as férias do colaborador Ivan a qual foram realizadas diversas portabilidades e ativação de número novo ao qual foram entregas responsavelmente dentro do prazo.

Até o momento a única hard skills de telefonia que não foi desenvolvida foi referente a configuração de ATA e Ramais e desbloqueio de IPs no fusion, ao qual será meu próximo objetivo dentro desse novo mês.


# Anlix
Do dia 24 de julho ao dia 30 de agosto foi necessário atualizar  o firmware e configurar manualmente o TR 069 de cada ONT Zyxel e dos Greatek 2100ac. Neste processo de atualização, foi identificado alguns problemas de referente ao roteador Greatek 1200ac ao qual não aceitava atualização de firmware e não era compatível com a configuração TR 069, mesmo após testes. Neste processo de atualização obtive o apoio do colaborador Thauan para atualizar e configurar os roteadores Zyxel e Greatek e do colaborador NOC IVAN para abstração e reconhecimento de problemas referente ao roteadores da Greatek.

Ainda neste período, assumi a responsabilidade nas descobertas de eventuais problemas referente ao anlix e os roteadores da Greatek, produzi um documento referente ao dia 21/08 e 23/08. Foi descoberto nestes testes que o greteak1200 ac possui algumas versões de firmware que não aceitam a atualização via IPV4, dessa forma algumas versões são impossibilitadas de serem atualizada remotamente, entretanto a faixa de firmware  **638.112.1.641** à **638.112.100.1523** aceita a configuração TR 069 e sobe no anlix e se mantém estável até a divulgação desse documento, exceto a versão 1376 que apresenta problemas no acesso remoto e deixa de compartilhar sua informações para o software Anlix. Ainda neste período de teste foi identificado por mim e pela equipe de teste e confirmado posteriormente pela Greatek que downgrades e upgrades de versões muitos distantes do Greatek 1200AC podem apresentar problemas quanto a integridade do aparelho, sendo necessário uma atualização de recuperação de firmware forçada.

# Aprimoramento
Do dia 24 ao dia 10, foi necessário o aprofundamento de conhecimento como administrador de redes, abordando mais afundo os protocolos e serviços como: NAT, CGNAT, ICMP, BGP, Abertura de portas, servidores e entre outros. Ainda neste prazo, tive o contato e aprofundamento com ferramentas de análise de redes como Wanguard, Grafana/Zabbix, Fusion, WireShark, MobaXterm, WinMtr, PingTracer, Paping, NMAP e entre outros. É importante ressaltar que parte dessa trilha de estudos, foi recomendada pelo NOC Alexandre.

# Monitoramento de Rede
Neste período, aprendi a analisar os incidentes e tratar o nível crítico de cada incidente, com o MobaXterm para acessar os Switches e OLTs, dessa forma era possível identificar possíveis problemas em portas, sinais  das mesmas e ausência de redundâncias além de utilizar software para viéis de debug de ligação. Contudo, neste período eu já manuseiava o wanguard e sabia identificar a origem e destino dos ataques sofridos a qual bloco de IP foi destinado e os tipos dos mesmos e relatar corretamente os incidentes comparando-os com o gráficos de variação de tráfego com os links de conexão do Grafana.

# Documentação
Neste prazo foi estritamente necessário, documentar os processos realizados pelos NOCs da qual participei dos procedimentos de telefonia e Anlix.

Devido a grande quantidade de documentos realizei a criação de um Ecossistema de tabelas relacionais "Brain NOC", este Ecossistema utiliza da ferramente notion para páginas e organizar a necessidade de notas de processos, registros de reuniões e atividades a serem executas. Além de proporcionar a criação de tabelas para verificação de atividades metrificadas.

# Fidelize
Grande parte dos meus esforços nesse período foi referente ao desenvolvimento do fidelize a qual o grande e principal problemas era a autenticação da API do hubsoft e a coletagem de dados para desenvolver a aplicação. No dia 20 de agosto em conjunto com o Eduardo foi apresentado um software para o CEO Renato ao qual coletava dados dos clientes do hubsoft de um determinado período e calcula as faturas pagas e convertia em pontos, essa aplicação possibilitava a exclusão, inserção e edição do dados da faturas de um determinado período, além de apresenta a páginas de gerenciamento da aplicação, apresentação, login e cadastro do usuário. O projeto continha, bootstrapp, html, css, tailwind CSS, PHP, Python e um banco de dados SQL para gerenciamento de dados.



 












