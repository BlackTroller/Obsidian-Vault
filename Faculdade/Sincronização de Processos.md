
- Threads e processos podem partilhar o mesmo espaço de endereçamento, segmentos de memória adicionais, ficheiros, . . .  **(processos cooperativos)**
- Acesso a recurso partilhado por mais do que um processo/thread em simultâneo 
	  → **Situação de competição** (ou race condition)
- Situações de competição resolve-se com coordenação da execução dos processos/threads que competem pelo recurso
	→ **Sincronização** da execução dos processos

#### Situação de competição

Situação em que o resultado da execução de vários processos que operam sobre um mesmo recurso é diferente dependendo da ordem de execução dos vários processos.

#### Problema da seção crítica

- Quando existem duas ou mais threads que usam ou alteram o valor de um objeto partilhado entre elas, diz-se que está numa secção crítica do seu código
- Se as threads executarem a seção critica em simultâneo, dá-se a incongruência de dados
- Situações que levem à incongruência devem ser evitadas
##### Solução para secção crítica

###### Requisitos

- **Exclusão mútua:** Se já existir uma thread a executar a secção crítica do código, mais nenhuma o poderá fazer
- **Progresso:** Se nenhuma thread está a executar a secção crítica, mas há várias que o querem fazer, então apenas estas últimas podem participar na seleção da thread que ir á executar a secção crítica naquele momento
	- Esta seleção não pode ser adiada indefinidamente
- **Espera limitada:** Deve existir um limite máximo para o número de vezes que se impede uma thread de aceder à secção crítica.

###### Problemas possíveis

- Com a implementação de condicionantes à execução decorrentes da existência de secções criticas, podem surgir 2 problemas

**Impasse ([[deadlocks]])**
Bloqueio de um conjunto de processos que aguarda por um evento que apenas pode ser gerado por um processo do conjunto.

**Míngua (starvation)**
Bloqueio de um processo enquanto espera indefinidamente pelo acesso a um recurso que não é libertado.

##### Soluções possíveis

- ***Soluções de software:***
	- Programador codifica a sua própria solução.
	- Recorrem a testes constantes de condições **(espera ativa)**

- ***Soluções de hardware:***
	- Utilização direta de instruções especiais do CPU
	- Cria dependência do CPU

- ***Soluções de sistema operativo:***
	- Sistemas operativos dispõem de funcionalidade avançadas para gerir secções críticas
	- Dependente do sistema operativo
	- Não obrigam à espera ativa

##### Soluções de software

**Algoritmo de Peterson**

![[algoritmo de peterson.png]]

Cumpre com os requisitos das secções críticas para dois processos num sistema mono-processador

##### Soluções de Sistema Operativo
###### Semáforo

- Mecanismo de sincronização que está presente na generalidade dos sistemas operativos;
- Funcionalidade resume-se a um número e 2 funções atómicas:
	- *wait():* obtém permissão e avança, senão bloqueia
	- *signal():* concede autorização
- *wait()* e *signal()* são executadas em exclusão mútua
- Número retrata a quantidade de processos que podem obter permissão em simultâneo

###### Semáforo - Impasse

- Assumindo que ***Sem1*** e ***Sem2*** são dois semáforos com o seu valor iniciado a 1
- Exemplo seguinte pode gerar um impasse (deadlock)
  
![[Semáforos - impasse.png]]

