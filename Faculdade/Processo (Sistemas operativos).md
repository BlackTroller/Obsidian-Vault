#### Definição de processo 

- Um **processo** é uma instancia de execução de um programa, executado num ambiente independente dos restantes. 

#### Programa vs. Processo 

- **Programa é um ficheiro**, no Sistema de ficheiros, passível de ser executado
- Programa é uma entidade passiva
- Processo é uma entidade ativa
- ***Processo necessita de recursos!***

#### Sistemas operativos como processo

- Sistema operativo pode ser visto com um conjunto de processos cooperativos, em execução concorrente
	- Processos gerados pelos utilizadores correm em modo não privilegiado ***(Sem acesso direto ao hardware)*** → **Modo utilizador**
	- Processos que fazem parte do sistema operativo correm em modo privilegiado ***(Com controlo total sobre ao hardware)*** → **Modo root**

#### Representação de um processo

- Informação utilizada por um sistema operativo para representar um processo e inclui, além do código do programa:
  
	- Dados das variáveis globais, locais, argumentos de funções, . . . (stack);
	- *Program counter* (ou instruction pointer) que indica qual é a próxima instrução a ser executada;
	- Recursos associados (tabelas de ficheiros, sinais, . . . )

#### Estados de um processo

Processos, desde que surgem e ao longo da sua existência vão transitando entre estados, até que terminam:

- **Novo (new):** Processo está a ser criado.
- **Execução (running):** Código do processo está a ser executado pelo processador.
- **Espera (waiting):** Processo pediu um operação de I/O e aguarda que esta esteja concluída.
- **Pronto (ready):** Processo está suspenso mas pronto para ser continuado.
- **Terminado (terminated):** Processo acabou.

![[diagrama de estados.png]]

#### Process control block (PCB)

- PCB é uma estrutura de dados usada pelo SO para guardar a informação de representação de um processo
- PCB estão armazenados em memória
- [[Sistemas Operativos]] tem sempre visão atual de cada processo

##### informação contida no PCB

- **Estado:** Estado do processo (new, ready, running, . . .)
- **Program counter:** Endereço da próxima instrução.
- **Registos CPU:** Guardados sempre que se suspende.
- **Escalonamento:** Prioridade, apontadores para filas de escalonamento, . . .
- **Memória:** Base e limite do segmento de memória, . . .
- **Contabilidade:** Tempo de CPU utilizado, utilizador, número do processo, tempo real utilizado, . . .
- **I/O:** Lista de ficheiros abertos, lista de sinais, . . .

#### Escalonamento de processos

- Sistemas multi-programados permitem a execução ***ao mesmo tempo*** de mais do que um processo
	- Requer capacidade para alternar entre processos ativos (em execução)
	- Só pode ser executado, em simultâneo, no máximo, um processo por núcleo (ou core)

- Pode-se escolher a **ordem de execução** dos processos!
- Quando um processo é criado este é **carregado para memória** principal e é colocado na **fila de processos prontos**
- Fila processos prontos contem todos os processos existentes no sistema que podem ser executados
- Filas podem ser implementadas como listas ligadas, como vetores, . . .
- Cada elemento destas listas tem a estrutura do PCB
- Fila processo prontos pode ser construída com dois apontadores (cabeça e cauda) do mesmo tipo

![[escalonamente de processos.png]]

##### Diagrama de Filas

- Durante a execução de um processo, pode:
	- Ser feito um pedido de I/O;
	- Acabar o tempo de CPU atribuído;
	- Criar um processo (filho);
	- Ser interrompido (sinal);

- Terminando o processo, o seu PCB é removido de todas as filas

![[diagrama de filas.png]]

#### Técnicas de escalonamento

- Processo, ao longo da vida, passa pelas várias filas de escalonamento
- Seleção de processos deve ser com base em lógica
- Seleção é efetuada pelo *dispatcher*
- Existem algumas abordagens:
	- Escalonamento de curto prazo *(short-term);*
	- Escalonamento de médio prazo *(medium-term);*
	- Escalonamento de longo prazo *(long-term)*

#### Escalonamento de curto prazo

- Técnica mais comum e, por vezes, a única disponível
- *Dispatcher* invocado com frequência muito elevada (ms)
- Tem de executar muito rapidamente (100ms ou menos)
- Limita a complexidade de escolha do próximo processo a executar
- Se *dispatcher* demorar 10ms e for executado a cada 100ms → 10% CPU utilizado para escalonamento!

---

#### Outro assunto

- Retrata o procedimento de substituição do processo ativo (em execução pelo CPU);
- Requer que se guarde o estado do processo atual e que se carregue o estado do novo processo a executar;
- Demora entre 1 a 1000 μs (quando implica a reposição do estado dos registos do CPU);
- Constantes mudanças de contexto e maior necessidade de processamento requerem novos mecanismos e técnicas → Tarefas (threads);

###### Troca de processo ativo num núcleo do CPU

![[troca de processo ativo.png]]


#### Dispatcher

- Componente responsável pelo escalonamento do CPU;
- Escolhe o próximo processo a executar;
- Efetua a mudança de contexto;
- Muda para o modo utilizador e posiciona-se na instrução seguinte;
- Tempo que demora chama-se ***dispatcher latency.***

#### Ciclo CPU-IO

- Processo mudam entre estes dois estado;
- Processo inicia com um ciclo de CPU (CPU burst inicial);
- Operação em alternância de ciclos de CPU com ciclos de E/S possibilita o escalonamento de processos

![[ciclo cpu-io.png#right]]

#### Tipos de escalonamento

O dispatcher executa quando:
1. Processo passa para Espera (solicita E/S);
2. Processo passa de Execução para Pronto (interrupção);
3. Processo passa de Espera para Pronto (E/S concluída);
4. Processo termina.
   
Existem dois tipos de escalonamento de curto prazo
- Preemptivo (situações 2 e 3)
- Não preemptivo (situações 1 e 4)

  ##### Preemptivo
  - Permite a suspensão temporária da execução de um processo;
  - Sistema operativo mantém o controlo
  - Requer mecanismos de controlo adicional
	  - Suspender processo a meio da escrita do ficheiro implica bloquear acesso ao ficheiro até que suspensão termine

##### Não Preemptivo
- Controlo é passado para o processo;
- Processo executa sistema operativo quando termina;
- Escalonamento muito simples de implementar;
- Não é adequado para os sistemas operativos atuais.

#### Critérios de escalonamento

- Algoritmos de escalonamento do CPU podem ser avaliados sob vários critérios;
- Dependendo do critério escolhido, um algoritmo pode ser considerado o melhor ou o pior;
- Não existe nenhum algoritmo ótimo.
###### Exemplos
- **Utilização do CPU** Quanto mais for utilizado o CPU, melhor. Valor em percentagem de tempo de utilização do CPU.
- **Rendimento** Número de processos concluídos por período de tempo.
- **Tempo de vida** Tempo desde que um processo inicia a sua execução até que termina.
- **Tempo de espera** Tempo gasto na fila de processos prontos e em filas de espera.
- **Tempo de espera inicial** Tempo gasto na fila de processos prontos pelo CPU burst inicial.

#### Algoritmos de escalonamento de CPU

- First-Come, First-Served  → Não preemptivo
- Shortest-Job-First → Não preemptivo
- Shortest-Remaining-Time-First → Preemptivo
- Prioridade → (Não) preemptivo
- Round-Robin  → Preemptivo
  
  
#### Processo Cooperativo
- Processo que partilha dados com outros processos e que, por isso, pode afetar ou ser afetado por estes.
	- Forma mais elementar de partilha de dados ocorre por partilha de memória;
	- Partilha de memória só está disponível para processos que executem no mesmo PC;
	- Não é possível entre processos que não usem o mesmo espaço de endereçamento de memória;
	- É necessário mecanismo alternativo de comunicação entre processos.

#### Formas de Comunicação

- Uma forma de comunicação entre processos que não partilhem memória pode ser conseguida com um mecanismo de troca de mensagens;
- Troca de mensagens pode ocorrer também entre processos a correr em equipamentos distintos;
- Internet, com os pacotes IP, é exemplo de um sistema de troca de mensagens global.

#### Sistema de troca de mensagens

- Funcionalidade elementar deste sistema é o de permitir comunicação entre processos, sem recorrer á partilha de memória
- Deve providenciar, pelo menos, as seguintes funções
	- *enviar(mensagem)*
	- *receber(mensagem)*
- Mensagens podem ter tamanho fixo ou variável
	- **Fixo** é mais fácil de implementar pelo sistema operativo
	- **Variável** é mais útil para quem desenvolve aplicações

###### Sistema de troca de mensagens (Ligação)

- Comunicação entre dois quaisquer processos requer que consigam mandar e receber mensagens entre eles
- Uma **ligação** entre estes é necessária
- Ligação pode ser implementada de muitas formas
- Existem fatores que afetam a forma como uma ligação é utilizada/implementada
	- Se a comunicação é **direta ou indireta**
	- Se a comunicação é **síncrona ou assíncrona**
	- Se a comunicação usa **buffering ou não**

#### Endereçamento

- Processos para comunicar, necessitam de uma forma de se identificarem (endereços)
- Uso de endereçamento tem impacto nos tipos de comunicação disponíveis
	- Comunicação direta
	- Comunicação indireta

##### Comunicação direta 
###### Endereçamento simétrico

- Em comunicação direta, cada processo comunicante t ˆem de explicitamente de identificar o outro processo
	- enviar(P,M) → Enviar mensagem M para processo P
	- receber(Q,M) → Receber mensagem M do processo Q
	- Denominado de endereçamento ***simétrico***

- Características deste tipo de ligação:
	- Processo necessitam conhecer endereços uns dos outros;
	- Ligação associada a exatamente 2 processos;
	- Só permite uma ligação entre 2 processos.

###### Endereçamento assimétrico

- Quando é permitido ao processo receber mensagens sem conhecer previamente o emissor, estamos perante endereçamento **assimétrico**
	- enviar(P,M) → Enviar mensagem M para processo P
	- receber(?,M) → Receber mensagem M de qualquer processo. Mensagem inclui identificação processo emissor

##### Comunicação indireta 

- Comunicação pode ser efetuada com recurso a armazenamento temporário
- Mensagens são armazenadas num **repositório** fora do processo
- Repositórios passam a ter endereços
- Dois processos comunicam partilhando um repositório:
	- enviar(R,M) → Enviar mensagem M para repositório R
	- receber(R,M) → Receber mensagem M de repositório R

###### Características
- Ligação só é estabelecida entre 2 processos se estes partilharem um repositório
- Ligação pode servir mais do que 2 processos
- Podem existir múltiplas ligações (repositórios) entre cada 2 processos

###### Utilização de repositório por mais do que 2 processos

Assumindo que
- Processos P1,P2 e P3 partilham o repositório A
- P1 envia mensagem para o repositório A
- P2 e P3 executam receber(A,M)
Quem recebe mensagem? → **Depende**
- Pode-se limitar partilha de repositório a 2 processos
- Pode-se impedir a execução simultânea de receber(A,M)
- Pode-se deixar o sistema escolher aleatoriamente

###### Autoridade sobre repositórios

- Repositórios podem pertencer ao sistema operativo ou ao processo
- Pertença ao processo:
	- Apenas o processo pode ler do repositório
	- Repositório é eliminado aquando do término do processo
- Pertença ao sistema operativo
	- Repositório tem existência própria
	- Requer funções de gestão de repositórios (criar, eliminar, editar, . . . )

#### Sincronismo

- Comunicação entre processos ocorre com a utilização das funções enviar() e receber()
- Estas funções podem ser implementadas adotando-se um **abordagem bloqueante (síncrona)** ou --**não bloqueante (assíncrona)**
###### Funções
- **enviar() bloqueante:** Função de envio só termina quando a mensagem é recebida pelo destinatário (processo ou repositório)
- **enviar() não bloqueante:** Função de envio termina mal acaba de enviar a mensagem
- **receber() bloqueante:** Função de receção só termina quando for efetivamente recebida uma mensagem pelo destinatário
- **receber() não bloqueante:** Função de receção verifica se existe mensagem, terminando de imediato (devolvendo a mensagem ou null)
  
- Qualquer combinação destas funções é possível
- Quando enviar() e receber() são bloqueantes
	- Dá-se o ***rendezvous*** dos processos
	- Ambos os processo têm de estar a executar em simultâneo para que se dê a comunicação

#### Buffering

- Capacidade de comunicação está associada a utilização de zonas de armazenamento de informação
- O armazenamento é temporário j á que acontece só até ao momento de leitura
- Zonas de armazenamento temporário são organizadas como filas (queues)
- Existem 3 tipos de filas:
	- Filas com capacidade zero
	- Filas com capacidade limitada
	- Filas com capacidade ilimitada

###### Filas com capacidade zero

- Fila tem 0 (zero) capacidade de armazenamento 
- Não é capaz de conter mensagens
- Emissor bloqueia até que a mensagem seja lida
- Implica o rendezvous
###### Filas com capacidade limitada

- Fila tem capacidade de armazenamento de algumas mensagens 
- Fila tem limite máximo de mensagens
- Se fila não estiver cheia, a mensagem é armazenada e o emissor pode continuar
- Se fila estiver cheia, emissor tem de aguardar até que seja libertado espaço para armazenar a mensagem
- Fila tem capacidade de armazenamento infinito
- Emissor nunca bloqueia na operação de envio de mensagem