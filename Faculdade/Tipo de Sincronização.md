![[Pasted image 20241014105209.png]]

#### Três tipos de interação: 
- ##### Comunicação síncrona 
	- O envio de uma mensagem é uma operação atómica que requer a participação de dois processos (emissor e recetor). 
	- Se o emissor está pronto a enviar a mensagem mas o recetor não a pode receber, o emissor bloqueia; 
	- Se o recetor está pronto a receber a mensagem mas o emissor não a envia, o recetor bloqueia.

- ##### Comunicação assíncrona
	- O emissor pode enviar a mensagem e continuar a executar sem bloquear, independentemente do estado do [[processo]] recetor; 
	- O recetor pode estar a executar quaisquer outras instruções, e mais tarde testar se tem mensagens a receber. Quando aceita a mensagem não sabe o que se passa no emissor (pode até já ter terminado).

- ##### Comunicação síncrona versus assíncrona (telefonar versus enviar uma mensagem)
	- ###### Síncrona
		- conceito de mais baixo nível (mais eficiente)
	- ###### Assíncrona
		- permite um maior grau de concorrência 
		- exige que o sistema de execução faça a gestão e o armazenamento das mensagens (um buffer de memória tem que estar preparado para armazenar um número de mensagens potencialmente ilimitado.
- ##### Invocação remota de procedimentos - RPC (Remote Procedure Call)
	- **A comunicação entre dois processos diz-se uma chamada de procedimento remoto quando:**
		- Um [[processo]] (o emissor) envia um mensagem;
		- O [[processo]] recetor produz uma resposta à mensagem; e 
		- O emissor permanece suspenso até à receção da resposta.
	- Do ponto de vista do [[processo]] emissor (cliente) este mecanismo funciona como a chamada de um procedimento. 
	- O procedimento não vai ser executado no próprio [[processo]] mas sim no recetor (servidor). 
	- Os dados comunicados na mensagem, funcionam como parâmetros do tipo valor.
	- A resposta do recetor pode ter a forma de parâmetros resultado.
	- O sistema de execução é responsável por encapsular sob a forma de mensagem qual o procedimento a executar e os respetivos parâmetros. A pós a execução do procedimento o resultado é uma mensagem do [[processo]] remoto para o cliente. 
	- O estado do procedimento não perdura entre invocações.

![[Pasted image 20241014111734.png]]

- ##### Invocação remota de procedimentos – Variante do RPC (callback)
	- ###### Emissor:
		- Após o envio da mensagem, o emissor prossegue a execução até que precise do resultado (permite maior concorrência); 
		- Se, nesse ponto, a resposta ainda não estiver disponível, o emissor é suspenso
	- ###### Recetor:
		- Quando um processo executa uma instrução de aceitação de mensagem, é suspenso até à chegada da mesma;
	- **Pode ocorrer que o recetor pretenda:**
		- escolher uma de entre um conjunto de mensagens possíveis; 
		- estabelecer condições para a receção de uma mensagem.
	- **Para isso é necessário que exista uma instrução em que o recetor:**
		- Seleciona uma de um conjunto de mensagens alternativas; 
		- Cada uma das quais pode ter associada uma condição para a aceitação da mensagem.

### Forma como são especificados os vários intervenientes no processo

#### Identificação dos [[Processo]]s

1.  Sistema que todos os processos têm um nome único
	 - O comando de envio pode nomear diretamente o processador recetor:
		 ENVIA mensagem PARA nome do processo 
	- Simetricamente no recetor
		Espera (mensagem) DE (nome do processo)
	- Se o recetor apenas estiver interessado em receber determinada mensagem, não importando quem é o emissor:
		- ESPERA (mensagem)                                // emissor é anónimo o receptor não

2. Quando não é apropriado um sistema de nomes únicos para todos os processos, definem-se entidades intermédias, ***caixas de correio*** (ou canais) conhecidas por ambos os intervenientes na comunicação
		ENVIA (mensagem) PARA (caixa de correio)
		ESPERA (mensagem) PARA (caixa de correio)

	- Uma caixa de correio pode ter várias formas. Pode ser usada por:
		- por vários emissores e vários recetores 
		- um emissor e vários recetores **(difusão ou “broadcasting”)**
		- vários emissores e um recetor 
		- um recetor e um emissor
		  
	- Pode ainda ser estruturada para enviar informação em ambas as direções ou apenas numa.








