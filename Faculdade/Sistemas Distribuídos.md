##### Sistemas Distribuído
- Conjunto de computadores ligados em rede, com software que permita a partilha de recursos e a coordenação de atividades, oferecendo idealmente um sistema integrado.
##### Computação distribuída
- a computação é dividida em várias unidades que executam concorrentemente em diferentes elementos de computação. Estes podem ser diferentes processadores em diferentes máquinas, diferentes processadores na mesma máquina, ou diferentes cores no mesmo processador.


Um sistemas distribuído é o resultado da interação de vários componentes que atravessam toda a stack de computação desde o Hardware até ao Software.

###### Características de um sistema Distribuído
- Comunicação através de mensagens
- Concorrência
- Partilha de recursos
- Sistema Assíncrono
- Falhas Independentes
- Heterogeneidade
	- Um Sistema Distribuído pode possuir:
		- Diferentes tipos de rede
		- Diferentes tipos de hardware
		- Diferentes [[Sistemas Operativos]]
		- Diferentes linguagens de programação

###### Desafios na implementação de sistemas distribuídos
- Escalabilidade
- Abertura (sistema aberto)
- Tolerância e Falhas
	- deteção da falha
	- localização da falha
	- mascarar/tolerar a falha
- Segurança
- Transparência
	- acesso
	- localização
	- concorrência
	- replicação
	- falhas
	- migração
	- desempenho
	- escalabilidade

###### Hardware
- Computador mais infraestrutura de rede; 
- O hardware é gerido pelo Sistema Operativo (SO) que fornece os serviços para: 
	- comunicação entre [[processo]]s (IPC – Inter Process communication)
	- escalonamento e gestão de [[processo]]s 
	- gestão de recursos, como o “file system” e periféricos

Requisitos para a confiabilidade:
- Disponibilidade (availability)
- Confiabilidade (reliability)
- Segurança (safety)
- Capacidade de manutenção (maintainability)