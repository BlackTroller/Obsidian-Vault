#### O que é um sistema operativo?

- Um sistema operativo é um programa de controlo que dever á suportar a interação entre os utilizadores e o hardware, permitindo-lhes executar programas de forma eficiente.
  
#### Primeiros computadores

- Surgiram no início da década de 1950;
- Visavam a usabilidade, a fiabilidade e o desempenho do hardware;
- Grandes dimensões;
- Utilizador era também o programador;
- Programas introduzidos por quadros de interruptores ou por cartões perfurados;

#### Monitores de controlo

- Não são considerados verdadeiros [[sistemas operativos]];
- Executava um utilitário ***(chamado de monitor)*** que permitia ao programador:
	- Tradutor para linguagem máquina **(assembler)**;
	- Editor de ligações **(linker)** → Acesso a rotinas de controlo de [[periféricos]];
	- Carregar programas para memória **(loader)**;
	- Executar programas;

- Partilha de recurso (todos!) por time-sharing
- Processador inativo frequentemente!
	- Espera pelo fim de operações dos [[periféricos]];
	- Espera por novos comandos do operador;

Exemplo de monitores de controlo
![[monitores de controlo.png]]

#### Tratamento por lotes (batch)

- Visava colmatar a ineficiência nas operações de E/S, adicionando:
	- Computador para preparação de dados e programas;
	- Computador para imprimir resultados;

- Execução sequencial de programas → **sem paragens**;
- Output de todos os programas surgia no final da execução de todos os programas;
- Programa era preparado e submetido → Execução sem interação com o utilizador **(background)**

![[tratamento por lotes.png]]

- Surgem [[periféricos]] de armazenamento de acesso aleatório (discos rígidos);
- Surge a técnica de ***spooling***:
	- Disco como armazenamento temporário **(buffer)** de operações sobre periféricos;
	- Permite sobreposição de operações de E/S;
	- Aumenta nível de desempenho global.

#### Multi-programação

**Definição de Multi-programação**
Intercalação de execuções distintas de um ou mais programas, armazenados em memória principal, por recurso a sinalização por interrupções.

- Técnica de ***spooling*** também pode ser aplicada aos programas
	- Requer sinalização adicional → Interrupções ou (interrupts).
- Possibilidade de escolher qual o próximo trabalho a executar → ***scheduling***

- Escalonamento de trabalhos implica:
	- Gestão de memória dos programas em execução;
	- Suporte para vários trabalhos em memória e em disco;
	- Suporte para a troca de trabalhos entre memória e disco;

- Surge a concorrência entre trabalhos
	- Gerir e controlar a comunicação e partilha de recursos entre trabalhos/processos

![[multi-programação.png]]

Vários sistemas evoluíram a partir dos sistemas multi-programados:
- Sistemas interativos;
- Sistemas paralelos;
- Sistemas distribuídos;

#### Multi-programação: Sistemas interativos

- Troca entre trabalhos efetuada com uma frequência muito elevada
	- Possibilita a interação entre o trabalho e o utilizador;
	- Suporta múltiplos [[utilizadores]];
	- Cria a impressão de que o utilizador é o único a usar a máquina;

- Mais complexos!
- Simultaneidade de trabalhos em memória
- Troca de trabalhos entre memória principal e disco ([[memória virtual]])
- Execução concorrente entre trabalhos

#### Multi-programação - Sistemas paralelos

- Utilizam mais do que processador (CPU)
- Partilham barramentos, relógio, memória, etc.
- Aumentam o desempenho e confiança no funcionamento sem falhas

- Multi-processamento simétrico:
	- Cada processador corre uma cópia do sistema operativo
	- Há a possibilidade de comunicação entre processadores

- Multi-processamento assimétrico:
	- Cada processador tem uma tarefa distinta
	- Processador Mestre que controla os restantes

#### Multi-programação - Sistemas distribuídos

- Distribuição do esforço de computação por vários computadores;
- Usam linhas de comunicação (rede, Internet);
- Partilham recursos (periféricos, ficheiros, etc.) entre locais;
- Aumenta a capacidade de computação;
- Permitem balanceamento de carga;
- Aumenta a segurança e estabilidade global;