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
