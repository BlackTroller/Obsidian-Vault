#### Testes de Caixa Branca
- Abordagem também conhecida por ***“teste estrutural”***, pois avalia o **comportamento interno dos componentes de software**
- Abordagem principalmente ***usada para a realização de testes unitários*** 
- Neste caso o *“tester”* tem **conhecimento da estrutura lógica interna do software a ser testado** 
- **Objetivo**: Determinar se todos os elementos lógicos e de dados nos componentes de software estão a funcionar adequadamente 
- O *“tester”* **define os casos de teste para determinar se existem defeitos** na estrutura do programa 
- O conhecimento necessário para esta abordagem **é adquirido nas fases posteriores do ciclo de vida do software, especificamente na fase de desenho.**

- **Conceber casos de teste segundo uma abordagem a testes de caixa branca.**
##### Critérios de Paragem
- Os “testers” necessitam de uma framework para:
- decidirem quais os elementos estruturais que devem seleccionar como foco para o teste
- escolher os dados de teste apropriado
- decidirem quando os esforços de teste são adequados e sucientes para poderem terminar o processo conantes de que o software funciona adequadamente 
- Mas quando parar?!

***Devemos parar um teste quando decidirmos que o software funciona de forma aceitável para o utilizador***

- Um **critério de adequação** de dados de teste é uma **regra de paragem** – as regras deste tipo podem ser usadas para determinar se ***os testes realizados são suficientes ou não.***
- O âmbito de aplicação do critério de adequação também inclui:
	- ajudar o “tester” a selecionar as propriedades de um programa que deve focar durante o teste
	- ajudar o “tester” a selecionar o conjunto de dados de teste para um programa baseado nas propriedades selecionadas
	- apoiar o “tester” com o desenvolvimento de objetivos quantitativos para teste

##### Critérios de Adequação
![[critérios de adequação.PNG]]

- Exemplos de dados de teste (critérios de adequação):
	- **exercitar os caminhos do programa da entrada até à saída**
	- **executar caminhos específicos derivados de combinações de fluxos de dados**, tais como definições e uso de variáveis
- O conceito de critério de adequação é o requisito que certas características ou propriedades do código serão executadas por casos de teste
	- **conduz-nos a uma abordagem chamada “análise de cobertura”**,a qual na prática é usada para estabelecer objetivos de teste e avaliar dados de teste
- No contexto de análise de cobertura **os “testers” referem-se frequentemente ao critério de adequação como “critério de cobertura”**

- Também apoiam os “testes de [[caixa preta]]"
- O objetivo do teste pode ser exercitar (cobrir) todos os requisitos funcionais ou todas as características do sistema.
- No entanto, contrariamente ao que acontece na abordagem de [[caixa preta]], os objetivos de cobertura de [[caixa branca]] têm forte apoio quer teórico quer prático.

##### Análise de Cobertura
- Análise de cobertura está tipicamente **associada com a utilização de modelos de controlo de fluxo** de dados para representar elementos estruturais e dados do programa
- Os **elementos lógicos** normalmente **considerados** para cobertura são baseados no fluxo de controlo do componente de software em teste
	- Expressões
	- Decisões / ramos (estas influenciam o fluxo de controlo do programa) 
	- Condições (expressões que avaliam verdadeiro/falso) 
	- Combinações de decisões e condições 
	- Caminhos (consequências de nodos nos gráficos de fluxo)

##### Elementos Lógicos
- Os gráficos de controlo de fluxo podem ser usados pelo “tester” para avaliar o código, e desenvolver casos de teste de caixa branca
- Num programa podemos ter:

![[elementos lógicos.PNG]]

##### Controlo de Fluxos
***Esta representação facilita o desenho de “testes de caixa branca”***

- Por questões de simplicidade, as expressões sequenciais são frequentemente omitidas ou combinadas num único bloco, que indica que se a 1ª expressão do bloco é executada, também são todas as que se seguem.
- Existem [[ferramenta]]s que geram estes gráficos
- Os “testers” podem usar [[ferramenta]]s para apoiar o desenvolvimento dos gráficos, especialmente para partes do código complexas

##### Cobertura de Expressões
- Vamos definir um possível caso de teste que satisfaz 100% da cobertura:
	- Todas as expressões (1 a 8) são executadas no caso de teste
	- **Note-se que**: podem existir diversos conjuntos de casos de teste que satisfaçam o critério…

![[cobertura de expressões.PNG]]

##### Cobertura de Condições
- Condition Coverage (Cobertura de Condições)
- desenhar casos de teste de tal modo que **cada resultado possível de cada condição, numa condição composta ocorre pelo menos uma vez**
- Exemplo:
	- decisão (i<N) AND (result <=maxint)
		- consiste em duas condições: (i<N) e (result <= maxint)
	- Devem ser desenhados casos de teste de tal modo que **cada condição assume o valor verdadeiro e falso pelo menos uma vez**
	- Note-se que os últimos casos de teste dos slides anteriores já garantem cobertura de condições (e ramos).
##### Cobertura de Caminhos Independentes
- Independent path coverage (Cobertura de caminhos independentes)
	- gerar um caso de teste para cada caminho independente
	- O número de caminhos linearmente independentes é dado pela McCabe’s cyclomatic complexity do programa V(G)

![[Pasted image 20241230145539.png]]

##### Cobertura de Caminhos
- Path coverage (Cobertura de caminhos)
	- executar todos os caminhos possíveis de um programa
	- critério de caixa-branca forte (baseado na análise de controlo de fluxo)
- Normalmente impossíveis: infinidade de caminhos (em caso de ciclo)
- Portanto, não são uma opção realística
- 
