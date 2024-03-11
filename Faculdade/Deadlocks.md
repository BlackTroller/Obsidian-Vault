- Conjunto de processos concorrentes que:
	- Detêm acesso exclusivo a recursos que outros necessitam 
	- Necessitam de recursos que outros detêm exclusivamente
- Processos envolvidos tipicamente entram em bloqueio permanente
- Uns impedem os outros de executar, e vice-versa
- Recursos podem ser físicos (impressora, espaço de memória, ...) ou lógicos (secção crítica, ficheiro, ...)
  
  ###### Exemplo de Deadlock
  
![[deadlock exemplo.png]]

#### Modelo Sistémico

- Sistema consiste num número finito de recursos, distribuídos por um conjunto de processos concorrentes
- Recursos agrupados por tipos:
	- R1, R2, ..., Rn;
	- Segmentos de memória, ciclos de CPU, ficheiros, dispositivos IO, ...

- Cada tipo de recurso poderá conter várias instâncias:
	- W1, W2, ..., Wn

- Sequência normal de utilização de recursos
	- **Solicitação** (Request) 
		- open(),fopen(), malloc(), alloc(), ...
	- **Utilização** (Use) 
		- read(), write(), fseek(), fread(),...
	- **Disponibilização** (Release)
		- close(), fclose(), free(), ...

- Imposta pelo sistema operativo por intermédio de systems calls
	- fread() dá erro se for usado sem o prévio fopen()

#### Condições necessárias para ocorrência deadlocks

1. ***Exclusão mútua*** (só um processo pode deter um determinado recurso em cada instante de tempo)
2. ***Retenção e espera*** (processo detentor de um recurso, espera por mais recursos detidos por outros processos)
3. ***Não preempção*** (recursos só podem ser libertados voluntariamente pelo processo detentor, quando terminar de o utilizar)
4. ***Espera circular***
	- Deve existir um conjunto de processos (P1, P2, ..., Pn) de tal forma que:
		- P1 aguarda pela libertação de um recurso detido por P2;
		- P2 aguarda pela libertação de um recurso detido por P3;
		- ...;
		- Pn aguarda pela libertação de um recurso detido por P1

![[espera circular.png]]

- ***Deadlock*** ocorre se, e só se, a condição de espera circular não tiver solução;

- ***Condição de espera circular*** não têm solução quando se verificam as condições anteriores;

- Três primeiras condições são necessárias, mas não suficientes para que se dê um situação de bloqueio.

#### Estratégias de tratamento de deadlocks

- **Prevenir**
	- Assegurar que pelo menos uma das 4 condições nunca se verifica
- **Evitar**
	- Não conceder recursos a um processo se tal se traduzir na possibilidade de bloqueio
- **Detectar e recuperar**
	- Conceder recursos sempre que solicitados e disponíveis;
	- Periodicamente, verificar se existem situações de bloqueio;
	- Caso existam, resolver a situação

#### Prevenir Deadlocks

- Garantir que pelo menos uma condição não se verifica
- **Exclusão mútua**
	- Muito difícil, se não impossível, obrigando à utilização de apenas recursos partilháveis
	- Certos recursos não podem ser partilhados
	- Existem técnicas que permitem minimizar, mas não eliminar, o problema
		- Impressoras e spooling ***(Espaço de disco não é ilimitado)***
- **Retenção e espera**
	- Garantir que quando um processo requisita um recurso não detêm mais nenhum
	- Requisitar todos os recursos antes de começar a executar
	- Requisitar recursos incrementalmente, libertando-os quando não conseguir requisitar mais
	- Leva à fraca utilização dos recursos
	- Implica o conhecimento prévio de todos os recursos necessários (não se adapta a sistemas interactivos)
	- Mantém-se a possibilidade de míngua (starvation)
- **Não preempção**
	- Possibilitar a preempção de recursos
	- Libertação de todos os recursos no momento da recusa de uma solicitação de recurso
	- Forçar à libertação de recursos solicitados por outros processos
	- Impossível se não se poder guardar o estado do recurso temporariamente (ex.: impressora, gravador de DVD, ...)
- **Espera circular**
	- Tipos de recursos são ordenados, sendo também solicitados pela mesma ordem 
		  (Ex: (1) Memórias, (2) Ficheiros, (3) Impressoras)
	- Caso um processo solicite um recurso do tipo Ficheiros, já só poderá solicitar recursos do tipo Impressoras
	- Caso um processo necessita de várias instâncias do mesmo recursos, deve solicitá-las todas de uma só vez
	- Ineficiente por impor uma sequência de solicitação de recursos, levando à negação desnecessária de acesso a recursos

#### Evitar deadlocks

- Permitir que as condições se verifiquem normalmente
- Analisar cada solicitação de recursos, caso a atribuição leve a uma situação de bloqueio, deve ser negada
- Examinar dinamicamente o estado global de alocação de recursos por forma a garantir que esperas circulares não sejam possíveis
- Duas estratégias para evitar deadlocks
	1. Não iniciar a execução de um processo se as suas necessidades (+ as já existentes) propiciar uma situação de bloqueio
	2. Não atribuir recursos adicionais, se isso propiciar uma situação de bloqueio

- Conceito base para evitar situações de bloqueio é o conceito de estado seguro
- Se o sistema é ***capaz de atribuir recursos a cada processo de forma a evitar situações de bloqueio***, então diz-se que está num ***estado seguro***
- Estado inseguro, é o que pode conduzir a uma situação de bloqueio\

![[evitar deadlocks.png]]

1. Estratégia
	- Inicio de execução de um novo processo é negado
	- Se as necessidades máximas de recursos do novo processo, mais as necessidade máximas dos processos já existentes
	- Não forem capazes de serem satisfeitas por qualquer um dos recursos
	- Estratégia simples de implementar mas muito restritiva
	- Leva a um fraco aproveitamento do sistema na sua globalidade

2. Estratégia
	- Não aceitar novas solicitações de recursos se isso possibilitar uma situação de bloqueio
	- Estratégia mais optimizada mas também mais complexa
	- Solução usual passa pelo teste de estado seguro
		- Verificar se o estado atual é ou não um estado seguro
	- Cenários de tipos de recursos com **uma única instância**, recorre-se a ***um grafo de alocação de recursos***
	- Cenários de **múltiplas instâncias** por tipo de recurso, recorre-se ao ***algoritmo do banqueiro***

##### Grafo de alocação de recursos

- Manter um grafo de alocação de recursos a processos
- Periodicamente procurar por ciclos (esperas circulares)
- Só funciona realmente se não existirem múltiplas instancias de cada tipo de recurso
- Caso existam ciclos, então existe a possibilidade de bloqueio

![[grafo 1.png|500]]

- Se existirem múltiplas instâncias de cada tipo de recurso
- Existência de um ciclo (espera circular) não implica forçosamente que se está perante uma situação de possibilidade de bloqueio

![[grafo 2.png|500]]

- **Vantagens:**
	- Menos restritivo que a prevenção de deadlocks
	- Não implica a requisição simultânea de todos os recursos necessários
	- Não obriga à preempção de recursos

- **Desvantagens:**
	- Necessita de processamento adicional para validar estados seguros
	- Implica o conhecimento antecipado de todos os recursos necessário

#### Detectar e recuperar deadlocks

- Recursos são atribuídos desde que estejam livres
- Periodicamente verifica-se a existência de bloqueios
- Caso existam, procede-se a recuperação
- Levantam-se alguns novos problemas
	- Quando efectuar a detecção de bloqueios?
	- Como efectuar a recuperação?

###### Quando efetuar a detecção de bloqueios?

- Sempre que se atribua um recurso...;
	- Consumo de CPU elevado e ,muitas vezes, desnecessário
- Periodicamente, com um intervalo de tempo fixo...;
- Quando existir pouca utilização do CPU...;
###### Como efectuar a recuperação?

1. Notificação do utilizador
	- Resolução do problema compete ao utilizador
2. Sistema recupera por si
	- “Matando” alguns processos para quebrar uma espera circular
	- Implementando preempção de recursos
###### Detecção (uma instância por tipo de recurso)

- Manter um grafo de dependências, entre processos, derivadas das necessidade de recursos (também conhecido como Wait-for Graph)
- Periodicamente procurar por ciclos, caso existam significam deadlocks

![[grafo 3.png]]

###### Recuperação

- **Alternativas de recuperação possíveis:**
	- Terminação de processos
	- Preempção de recursos

- **Terminação de processos:** 
	- Termino abrupto de todos processos encravados
	- Termino sequencial de processos encravados até que termine o bloqueio
		- Que ordem utilizar na terminação de processos? Que factores considerar na definição dessa ordem?
			- Prioridade, tempo de CPU consumido, recursos usados, tipo de processo, etc
	
	- Executar o algoritmo de detecção após cada término forçado de processo

- **Preempção de recursos**
	- Retirar sequencialmente recursos aos processos até que termine o bloqueio
	- Por quais recursos/processos começar?
		- Considerar factores de ponderação como o número de recursos detidos, etc.
	- Que acontece aos processos aos quais se retiram os recursos a meio da sua utilização?
		- Suporte para rollback? (muito difícil)
	- Como impedir a míngua?
		- Risco de ser sempre o mesmo a “sofrer”

#### Estratégia combinada

- Assumindo que nenhum dos métodos é sempre bom
- Dependendo do cenário, os resultados variam de estratégia para estratégia
- Combinar as várias estratégias
- Aplicar a que produzir o melhor resultado para cada tipo de recursos

#### Ignorar a existência de deadlocks

- Estratégia utilizada pelo sistema UNIX
- Considera-se que o custo de consumo de CPU para prevenir / evitar / detectar bloqueios não é compensador
- Negam-se pedidos se não existirem recursos disponíveis
- Funciona razoavelmente bem, se os deadlocks ocorrerem essencialmente nos processos de utilizador e não nos processos de sistema