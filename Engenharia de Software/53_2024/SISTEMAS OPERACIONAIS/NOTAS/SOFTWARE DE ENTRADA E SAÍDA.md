O software de E/S não se resume a drivers. Existem **quatro camadas** para comunicação entre dispositivos e o sistema operacional:
  1. **Tratadores de interrupção**: Bloqueiam o driver até a conclusão da operação de E/S.
	  1. **Exemplo**: No Linux, o tratamento de interrupções para uma placa de rede envolve um tratador de interrupção que bloqueia o driver da placa até que a transmissão ou recepção de dados seja concluída. Isso garante que a CPU seja notificada e possa processar os dados quando a placa de rede sinaliza que a operação foi concluída.
  2. **Drivers de dispositivo**: Cada dispositivo precisa de um driver específico para comunicação. Ex: Linux tem 60% do código voltado para drivers.
	  1. **Exemplo**: O driver de impressora é um código específico que permite que o sistema operacional se comunique com uma impressora. Esse driver traduz as instruções do sistema operacional em comandos que a impressora pode entender.
  3. **Software de E/S independente de dispositivo**: Interface para operações comuns (buffer, erros, alocação de recursos).
	  1. **Exemplo**: A biblioteca de funções `libc` em sistemas Unix fornece funções como `fread` e `fwrite` para operações de leitura e escrita de arquivos, sem se preocupar com o tipo de dispositivo subjacente (por exemplo, disco rígido ou SSD).
  4. **Softwares de E/S do espaço do usuário**: Usam bibliotecas específicas e estão no nível do usuário, diferentemente dos drivers que são do núcleo do sistema.
	  1. **Exemplo**: Um editor de texto como o Microsoft Word usa bibliotecas de entrada/saída para salvar e abrir arquivos. Essas bibliotecas são específicas para o Word, fornecendo funções personalizadas para manipular documentos, mas dependem das bibliotecas do sistema operacional para a comunicação com o hardware.

### Exemplos de Dispositivos de E/S:
- **Disco rígido**: Dispositivo de blocos. Sua comunicação é via ponte sul (southbridge).
- **Temporizadores**: Controlam a data/hora e o uso da CPU (ex.: escalonamento round-robin), garantindo que processos não monopolizem a CPU.

### Economia de Energia
- **Monitores** e **discos rígidos** são os maiores consumidores de energia. Para reduzir o consumo, sistemas operacionais oferecem funções de hibernar/suspender, economizando energia ao desligar dispositivos inativos.

# Questões Conceituais
#Sistemas_Operacionais/Conceitos 

Quais são as quatro camadas do software de entrada/saída?
??
1. **Tratadores de Interrupção**: Garantem que o driver que iniciou a operação de entrada/saída seja bloqueado até sua conclusão.
2. **Drivers**: Código específico para controlar cada tipo de dispositivo de entrada/saída.
3. **Softwares de Entrada/Saída Independente do Dispositivo**: Fornecem funções comuns como armazenar no buffer e reportar erros.
4. **Softwares de Entrada/Saída do Espaço do Usuário**: Trabalham no nível do usuário, usando bibliotecas personalizadas para funções específicas.
