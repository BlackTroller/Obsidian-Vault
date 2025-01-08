Ao nível do [[Sistemas Operativos]], a comunicação entre processos é implementada usando protocolos: 
- ***TCP/IP*** (Transmission Control Protocol / Internet Protocol); 
- ***UDP*** (User DatagramProtocol); 
- Outros. 
  
  
Acima do SO, existe o ***middleware*** que constrói uma camada de abstração que permitirá às aplicações abstraírem-se da heterogeneidade do hardware e do próprio sistema operativo. 

O ***middleware*** fornece uma interface uniforme para o desenvolvimento de aplicações.

![[Pasted image 20241014103236.png]]

A ***comunicação entre processos (IPC)*** é usada para transferir dados entre os [[processo]]s e para coordenar a sua atividade.

Modelos de IPC mais importantes:
- **Memória partilhada** 
- **Comunicação por mensagens**

##### Sistemas de Memória Partilhada
- Os [[processo]]s acedem a um único espaço de endereçamento;
- Comunicação através de variáveis partilhadas; 
- Sincronização feita pelas técnicas clássicas da programação concorrente (ex. Semáforos ou Monitores).

##### Sistemas de Memória Distribuída
- Vários espaços de endereçamento disjuntos **(cada processador tem a sua própria memória local)** 
- Comunicação por mensagens (através de uma canal de comunicação)
- Comunicação e sincronização integradas num único conceito
  
O programador utiliza os **mecanismos de comunicação** por mensagens sem se preocupar com a forma como é feito o **armazenamento** e a **transferência dos dados**.

#### Modelos de sincronização por Mensagem

As várias formas de comunicação por mensagens distinguem-se por:

1. **Tipo de sincronização (ou interação):** 
	- ***Comunicação síncrona*** 
	- ***Comunicação assíncrona***
	- ***Invocação remota de procedimentos***

2. **Forma como são especificados os vários intervenientes no processo:**
	- ***Identificação de processos***
	- ***Criação dos processos (dinâmica e estática)***
	- ***Comunicação bidirecional ou unidirecional***


