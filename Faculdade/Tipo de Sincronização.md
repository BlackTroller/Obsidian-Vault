![[Pasted image 20241014105209.png]]

#### Três tipos de interação: 
- ##### Comunicação síncrona 
	- O envio de uma mensagem é uma operação atómica que requer a participação de dois processos (emissor e recetor). 
	- Se o emissor está pronto a enviar a mensagem mas o recetor não a pode receber, o emissor bloqueia; 
	- Se o recetor está pronto a receber a mensagem mas o emissor não a envia, o recetor bloqueia.

- ##### Comunicação assíncrona
	- O emissor pode enviar a mensagem e continuar a executar sem bloquear, independentemente do estado do processo recetor; 
	- O recetor pode estar a executar quaisquer outras instruções, e mais tarde testar se tem mensagens a receber. Quando aceita a mensagem não sabe o que se passa no emissor (pode até já ter terminado).

- ##### Comunicação síncrona versus assíncrona (telefonar versus enviar uma mensagem)
	- **Síncrona**
		- conceito de mais baixo nível (mais eficiente)
	- **Assíncrona**
		- permite um maior grau de concorrência 
		- exige que o sistema de execução faça a gestão e o armazenamento das mensagens (um buffer de memória tem que estar preparado para armazenar um número de mensagens potencialmente ilimitado.