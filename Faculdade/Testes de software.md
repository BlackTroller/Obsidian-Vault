Os [[testes de software]], são uma **forma dinâmica** de ***verificar*** se o programa, através de um conjunto de **testes finito***, age de acordo com o esperado. **Executar testes de software de forma dinâmica**, significa **executar testes para uns determinados valores de entrada**, pré-definidos. Existem, também, formas de **testes estáticas**, que são usadas em **testes de qualidade de software**.

É importante considerar que, às vezes, os ***valores de entrada, (sozinhos),*** podem ser **insuficientes** para concluir se o software opera de acordo como o planeado. Mesmo um pequeno programa possui um número **finito de testes possíveis** de serem executados. Realizar testes pode ser uma tarefa exaustiva, daí na prática o ***número de testes a executar é infinito, por esse motivo, são normalmente usados critérios de restrição aos números de testes***.

Esses **critérios** são, às vezes, difíceis de escolher. Quanto ***melhor forem os critérios mais eficazes serão os testes***, mas, como foi dito anteriormente, essa escolha é difícil de se fazer. Usam-se, **estratégias de análise de risco** e recorre-se a **técnicos especializados** de desenvolvimento de software para auxiliar as equipas de testes a **restringir as condições de teste**. Quando se realizam testes, esperam-se, uns determinados ***valores de saída, conforme os valores de entrada***.
Atualmente, está a haver uma mudança no pensamento das equipas de desenvolvimento de software em relação aos testes. No passado, os testes de software só eram efetuados no **final do desenvolvimento do software**, em contraste, hoje em dia, os **testes de software** são uma parte crucial do ciclo de vida do desenvolvimento do programa.
O [[SWeBoK]] defende que o ***planeamento dos testes deve de começar logo nas fazes primordiais de desenvolvimento de software***, na escolha dos **requisitos do [[processo]]**, assim garantido também a qualidade deste.

**É importante fazer referência, à propriedade iterativa dos testes**, ***não são estanques, mas sim um [[processo]] evolutivo e que acompanha o desenvolvimento do [[produto]]***, e não deve de ser estático. Para muitas empresas a melhor abordagem é garantir a **prevenção de erros**. 
Então podemos concluir que os [[testes de software]] são uma **abordagem preventiva e focada na qualidade final** e são um bom indicador e uma boa forma de desenvolvimento de software. Claro que mesmo assim podem haver erros no [[produto]] final, é algo que as equipas de manutenção de software devem de abordar. Existem **técnicas estáticas e técnicas dinâmicas para os testes de software**.

É importante lembrar que, nem todos os [[método]]s descritos são aconselháveis para todos os softwares e nem todos as **técnicas** de teste foram listadas.
Para identificar que tipo de teste efetuar, o ***“test target“***, ou seja, os **objetivos e os critérios**, são o suficiente. Para saber quantos testes são necessários realizar para alcançar o nosso **objectivo**, usa-se o ***“critério de adequação software“***, através deste conseguimos saber quantos testes temos de realizar para conseguir cumprir o nosso objetivo. Para se conseguir responder à pergunta, que testes efectuar, usam-se ***“critérios de seleção“***, assim consegue-se ter **mais ou menos uma noção de o quê testar e como**.

1. ***ERROS vs DEFEITOS:*** 
	   Termos com o **intuito de distinguir o problema** no nosso software, e a sua origem ***(o defeito e o erro, respetivamente)***. Na teoria, **há erros que podem não afetar o nosso software**; os ***“problemas“*** no desenvolvimento de software funcionam de **forma reativa e não pró-ativa**, se ninguém encontrar o defeito, o software não tem defeitos. ***Por esse mesmo motivo é que é importante, sempre que se encontram defeitos, remover os mesmos***. Também é possível uns erros estarem a encobrir outros e uns defeitos a encobrir outros também. É necessário ter em muita atenção as primeiras fases de desenvolvimento de software, ***se não se conhecer bem o domínio, o negócio, as intenções das partes envolventes, etc…*** podem haver **erros de raciocínio** que levam a defeito. É tudo relativo, não há nenhuma norma ou convenção para especificar que terminologia usar, para simplificar iremos considerar que os **defeitos são os famosos** ***“bugs“*** **e os erros, são erros no raciocínio que provocam defeitos**. O [[SWeBoK]] diz que existem **erros, faltas, fracassos, defeitos…e mais.** 
2. ***Critérios de seleção de testes e critérios de adequação de software:*** 
	   Como dito a cima, **critérios de seleção de testes** servem para selecionar que tipos de [[metodologia]] de teste deve de se usar relativamente ao que pretendemos testar e ao software que temos. **Critérios de adequação de software**, são critérios, que os engenheiros de software e as equipas de teste escolhem para poder efetuar os testes.
3. ***Eficácia e Objetividade:*** 
	   A **eficácia** do teste é determinada pela **observação de alguns testes e a sua performance**. Os testes a efetuar dependem dos objetivos, dito isto a **eficácia dos testes está dependente dos objetivos, quanto mais especificados os objetivos mais eficaz será o nosso teste**.
4. ***“Testing for defect discovery“ ou Testar orientado a erros:***
	   Um **teste bem sucedido é aquele que faz com que o teste falhe** (nota o objetivo dos testes é falhar), ou seja **o objetivo deste teste é, ambiente realístico, conseguir testar o sistema, de forma a que não haja nenhum defeito**, e demonstrar que o software cumpre os requisitos e os objetivos traçados.
5. ***“The oracle problem“ ou teste oracle:*** 
	Um **“oracle“** é um ser humano, ou algo **mecanizado** que averigua, de acordo com se o software ***“passa“*** ou ***“falha“*** de acordo com uns requisitos específicos. Existem muitos tipos de **teste oracle**, pode-se fazer um **teste para ver se ele cumpre os requisitos**, para ver se o programa vai de acordo com uns comportamentos esperados numa determinada situação, ou ainda, se a documentação é a correta. Fazer um ***“oracle“*** automatizado é dispendioso, não é uma opção viável para equipas com um orçamento pequeno.
6. ***Limites práticos e teóricos dos testes de software:***
	   A **teoria dos testes** alerta para o facto de **não ser bom, numa serie grande de testes, serem todos bem sucedidos**. ***“Unfortunately, most established results of testing theory are negative ones, in that they state what testing can never achieve as opposed to what is actually achieved.“*** Isto significa que, por exemplo o algoritmo Dijkstra para o aforismo (regras) do software, **é capaz de encontrar defeitos**, mas não funciona se não houver defeitos, então é necessário efetuar testes com cuidado e também usar **técnicas de gestão de risco**, o [[SWeBoK]] diz que os testes se fazem através de risco.
7. ***O problema dos caminhos impossíveis:***
	   **Caminhos impossíveis** são caminhos que **não conseguem existir, independente dos valores de entrada.** São um grande problema no **design de testes com base em mapeamento de caminhos**, especialmente se esses mecanismos de testes forem ***automatizados***.
8. ***Testabilidade:***
	   O termo a ***“testabilidade do software“*** em engenharia de software pode ter dois significados: pode significar que o software é **fácil de testar tendo em conta os critérios definidos** para o testar ou ***ainda a possibilidade de medir, estatisticamente, a probabilidade*** que um caso de testes tem de **falhar ou ser bem sucedido**, ambos os significados são importantes.

#### O especialista de Testes

- Alguém cuja formação está baseada nos princípios, práticas, e [[processo]]s que constituem a disciplina de [[engenharia de software]], e cujo, foco específico está na área de ***“software testing”***.
- Deverá ter conhecimento de princípios relacionados com testes, [[processo]]s, medidas, standards, planos, [[ferramenta]]s, e [[método]]s, e deverá aprender como aplicá-los às tarefas de teste a serem executadas

#### O papel de ‘[[Processo]]’ na qualidade de SW...

* Processo, no domínio da engenharia de software é:
	* o conjunto de **[[método]]s, práticas, standards, documentos, atividades, políticas, e procedimentos** que os engenheiros de software usam para desenvolver e manter um sistema de software e os seus artefactos associados, tais como planos de projeto e teste, documentos de projeto, código e manuais.

##### Processo de desenvolvimento de SW e Testes
- No processo de desenvolvimento de software existem vários processos incluindo o "[[Testing]]"
	- Está relacionado com outros dois processos:
		- **Verificação (Foco no [[Processo]])**
			- É o processo de avaliar um sistema ou componente de software para determinar se os produtos de uma determinada fase de desenvolvimento satisfazem as condições impostas no começo dessa fase (associado a atividades de inspeção, revisão)
		- **Validação (Foco no [[Produto]])**
			- É o processo de avaliar um sistema ou componente de software durante, ou no final, do ciclo de desenvolvimento para determinar se satisfaz os requisitos especificados


#### Modelo de maturidade de testes de SW

![[modelo de maturidade.PNG]]

##### Conceitos e definições básicos

###### Erros

- Um **erro** é um engano, uma ideia errada/equívoco, ou interpretação errada/má compreensão por parte de um *“desenvolvedor”* de software
- Na categoria de *“desenvolvedor”* incluímos engenheiros de software, programadores, analistas e os testers.
	- Exemplo: um *“desenvolvedor”* entender mal a notação de desenho, um programador digitar o nome de uma variável incorretamente
###### Defeitos (Faults/Defects)

- Um **defeito** é introduzido no software como resultado de um **erro**. É uma anomalia no software que pode fazer com que este se comporte incorretamente, e não conforme a sua especificação.
- São por vezes chamados *“bugs“* 
- O uso do termo *“bug”* trivializa o impacto do defeito em termos da [[qualidade]] de software... 
- O uso do termo **defeito** está também associado com artefactos de software, tais como documentos de requisitos e projeto 
- Os **defeitos** que ocorrem nos artefactos são causados por erros e são normalmente detetados no [[processo]] de revisão.

###### Falha/Fracasso (Failure)

- Fracasso é a **incapacidade de um sistema ou componente de software executar as funções que lhe são requeridas**, dentro dos requisitos de desempenho especificado 
- Por ***exemplo***, durante a execução de um componente ou sistema de software, um tester, “desenvolvedor”, ou utilizador ***observa que este não produz os resultados esperados***.
- Comportamento incorreto pode incluir produzir valores incorretos para variáveis de saída, etc...
- Um defeito no código não produz sempre um fracasso...
- ***Na realidade, software defeituoso pode operar durante grandes períodos de tempo sem exibir qualquer comportamento incorreto.***


- Qual abordagem usual para detetar defeitos numa parte de software? .... 
- Para decidir se o software passa ou não no teste, o tester precisa de conhecer os outputs para o software, dado um conjunto de inputs e condições de execução 
- O Tester junta esta informação num item chamado ***“caso de teste“***
- Um **caso de teste** é num sentido prático um item relacionado com teste, que contem a seguinte informação 
	- **Um conjunto de entradas de teste**: são dados recebidos de uma fonte externa pelo código em teste. A fonte externa pode ser hardware, software, ou humana
	- **Condições de execução**: são condições requeridas para executar o teste, por exemplo, um certo estado de uma base de dados, ou uma configuração de um dispositivo de hardware 
	- **Saídas esperadas**: São os resultados especificados para serem produzidos pelo código em teste.


###### O que é um teste?
- •É um grupo de casos de teste relacionados, ou um grupo de casos de teste e procedimentos relacionados 
- **Test Oracle** : É um documento, ou parte de software que permite aos testers determinar se um teste passou ou falhou (um programa, ou um documento que produz ou específica o resultado esperado de um teste, pode servir como um oracle) 
- **Test Bed**: é um ambiente que contém todo o hardware e software necessário para testar um componente de software ou um sistema de software 
	- Este incluí o ***ambiente de teste completo***, ou seja, tudo o que e necessário para apoiar a execução dos testes (por exemplo: simuladores, [[ferramenta]]s de software, etc....)

![[conceptTeste.PNG]]


![[conceptTeste2.PNG]]

###### Testes Unitários
- **Os diversos componentes são codificados e testados de forma isolada**, garantindo assim a respetiva correção interna. Incidem sobre parcelas do sistema, e são realizados por cada programador de forma independente.
	- Testes baseados na experiência, especificações e código;
	- O principal objetivo é detetar defeitos funcionais e estruturais em parcelas de código.

###### Testes de Integração 
- **testes parcelares, que vários programadores realizam conjuntamente** com vista a garantir que vários componentes interactuam entre si de forma adequada.
	- Testes de grupos integrados de componentes, integrados para criar um subsistema;
	- O principal objetivo é detetar defeitos que ocorrem nas interfaces das unidades e no seu comportamento comum.

###### Testes de Sistema
- **testes globais em que todos os componentes do sistema são integrados**; possibilitam a verificação da conformidade do sistema com todos os requisitos definidos.
	- Normalmente são da responsabilidade de uma equipa de teste independente; 
	- São normalmente baseados num documento de requisitos (requisitos/especificações funcionais e requisitos de [[qualidade]]);
	- O principal objetivo é avaliar atributos tais como usabilidade, fiabilidade e desempenho (assumindo que os testes unitários e de integração foram realizados);

###### Testes de Aceitação
- testes formais que os utilizadores realizam sobre o sistema. Quando o sistema passa este (difícil!!!) teste, o cliente deverá aceitar o sistema como ***“pronto”*** e consequentemente este pode ser colocado em produção, ou operação, efetiva.
	- O principal objetivo é avaliar se o produto vai de encontro aos requisitos do cliente e expectativas.

**Ciclo de vida dos testes**
![[ciclo de vida dos testes.PNG]]

##### Tipos de Testes
- **Testes de desempenho**: permitem analisar o tempo de resposta do sistema e, dum modo geral, verificar o nível de utilização de recursos disponíveis
- **Testes de usabilidade**: permitem analisar a adequabilidade do desenho das interfaces homem-máquina e constatar se o sistema é fácil de utilizar 
- **Testes funcionais**: permitem determinar a correção da implementação de funcionalidades, conforme especificadas pelos correspondentes requisitos funcionais 
- **Testes de segurança**: nos testes de segurança estamos à procura de um comportamento anómalo que não sabemos quando acontece….Precaver contra ataques; Garantir robustez do software face a determinados ataques típicos; Detetar vulnerabilidades; Preparar medidas de contingência; Oferecer maior valor acrescentado ao cliente; …
- **Testes de robustez**: o objetivo é determinar o comportamento de um sistema em situações hostis. Normalmente pensados em conjunto com os testes de segurança.
- **Testes de fiabilidade**: o objetivo é avaliar a capacidade de um sistema de software desempenhar as suas funções sob determinadas condições num determinado período de tempo.

##### Do plano ao Relatório
###### Preparação dos testes
- **Test Plan; Test Design Specication; Test Case Specication; Test Procedure; Test Item Transmittal Report**
###### Execução dos testes
- Test Log; Test Incident Report
###### Finalização dos testes
- Test Summary Report

![[testSummaryReport.PNG]]

#### Documentação relacionada como testes

##### IEEE 829 - Test Plan
- what has to be done
- to what quality standard
- with what resource
- to what time scale,
- and outlines the risk how they would be overcome

##### IEEE 829 - Test Design specification
- the first stage in developing the tests for a software testing project
- derived from the documents that come into the testing stage, such as requirements and design 
- records which features of a test item are to be tested, and how a successful test of these features would be recognize 
- The test design does not record the values to be entered for a test, but describes the requirement for defining values

##### IEEE 829 - Test Case Specification
- The test cases are produced when the test design is completed. Test cases specify for each testing requirement:
	- The exact input values that will be input and the values of any standing data that is required 
	- The exact output values and changes of value of the internal system state that are expected and any special steps for setting up the tests 
- A feature from the Test Design may be tested in more than one Test Case, and a Test Case may test more than one feature. The aim is for a set of test cases to test each feature from the Test Design at least once.

##### IEEE 829 - Test Procedure Specification
- developed from both the Test Design and the Test Case Specication. 
- describes how the tester will physically run the test, the physical set-up required, and the procedure steps that need to be followed 
- The standard defines 10 procedure steps that may be applied when running a test.

##### IEEE 829 - Test Item Transmittal Report
- In User Acceptance Testing this may be the completion of System Testing.
- It describes the items being delivered for testing, where to nd them, what is new about them, and gives approval for their release

##### IEEE 829 - Test Log
- The Test Log records the details of what Test Cases have been run, the order of their running, and the results of the test 
- The results are either the test passed, meaning that the actual and expected results were identical, or it failed and that there was a discrepancy

##### IEEE 829 - Test Incident Report
- The report consists of all details of the incident such as actual and expected results, when it failed, and any supporting evidence that will help in its resolution. The report will also include, if possible, an assessment of the impact upon testing of an incident. 
- Includes the expected results being wrong, the test being run wrongly, or inconsistency in the requirements meaning that more than one interpretation could be made.

##### IEEE 829 - Test Summary
- The Test Summary brings together all pertinent information about the testing, including an assessment about how well the testing has been done, the number of incidents raised and outstanding, and crucially an assessment about the quality of the system. Also recorded for use in future project planning is details of what was done, and how long it took
- This document is important in deciding whether the quality of the system is good enough to allow it to proceed to another stage

#### Plano de testes
- **Norma ANSI/IEEE 829-1998** para Documentação de testes de software define plano de testes como: 
	- Um documento que define o **âmbito, abordagem, recursos e escalonamento** (planeamento) **das atividades de teste previstas**. Identifica ***itens de teste, as funcionalidades*** a serem testadas, as tarefas de teste, quem executará cada tarefa, e quaisquer riscos que requeiram planos de contingência
- Planos de teste são **documentos extensos**, normalmente compostos por vários documentos mais pequenos

- **O plano de testes como um [[produto]]**
	- Um bom plano de testes ajuda a organizar e gerir o esforço de teste 
	- Muitos planos de teste ultrapassam este âmbito, e tornam-se num produto por si só 
	- A estrutura, formato, e nível de detalhe são determinados não só pelo que se entende como mais apropriado para eficácia das tarefas de teste, mas também pelos requisitos do cliente ou entidade reguladora

- **Plano de testes: [[Produto]] ou [[Ferramenta]]?**
	- O que os clientes normalmente querem é programas que funcionem corretamente 
	- Os clientes tipicamente não estão interessados nos testes efetuado 
	- Os clientes estão interessados na forma como o programa funciona 
	- Para estes clientes, o plano de testes não é um produto 
	- Um plano de testes é uma ferramenta valiosa na medida em que ajuda a gerir o projeto de testes e a encontrar falhas do programa.

- **O Plano de testes como uma [[Ferramenta]]
	- A norma ***ANSI/IEEE 829*** requer
		- especificações da conceção de testes 
		- especificação dos casos de teste 
		- registos de teste 
		- especificação dos procedimentos de teste 
		- relatórios dos teste 
		- especificações de entrada/saída 
		- especificação de requisitos de procedimentos especiais 
		- notas sobre a dependência entre casos
		- listas de documentos a serem elaborados após testes 
		- escalonamento (planeamento) dos testes 
		- planeamento de recursos humanos 
		- lista (escrita) de responsabilidades de cada elemento da equipa 
		- critérios para a suspensão e reativação dos teste

- **Secções do plano de testes (IEEE Standard 829)** 
	- Identificador do plano de testes 
		- Nome ou número único, que identifica o projeto 
	- Introdução 
		- Descrição do objetivo do plano de testes. Inclui referências a todas as 
		- normas e documentos relevantes na definição da política seguida 
	- Itens de teste 
		- Lista de todos os componentes do programa ( função, módulo, classe, método, etc.) que vão ser testados, incluindo os documentos de referência. Se apropriado, listar o que **NÃO** vai ser testado 
	- Características a serem testadas 
		- Referenciadas às especificações do desenho (conceção) do teste 
	- Características que não vão ser testada 
		- Quais, e porquê.

###### Em Resumo
- **A documentação de teste facilita a tarefa de teste**
	- Para criar um bom plano de teste, é necessário investigar o programa de forma sistemática à medida que se vai desenvolvendo o plano
	- O tratamento do programa torna-se mais claro, mais exaustivo, e mais eficiente
	- A documentação de testes facilita a comunicação sobre as tarefas e o processo de teste
	- A documentação de teste fornece uma estrutura para organizar, escalonar (planear) e gerir o projeto de teste
- **Desenvolvimento inicial do material de teste**
	- Primeiros passos para desenvolver um plano de testes
		- Testar contra a documentação (especificação, manual, ...)
		- Criar uma documentação que seja organizada para facilitar testes eficientes, por exemplo uma lista de funções
		- Fazer uma análise simples de limites
			- Testar valores limite em todas as situações em que se podem fornecer dados
- **Onde focar a seguir**
	- Erros mais prováveis
	- Erros mais visíveis (para o utilizador)
	- Áreas do programa mais usadas
	- Área do programa mais referida como distintiva
	- Áreas mais difíceis de corrigir
	- Áreas melhor compreendidas
	- Testar tão cedo quanto possível
	- Escrever os casos de teste antes do software ser testado
		- aplicar-se a qualquer nível: unidade, integração e sistema 
		- ajuda a obter conhecimento sobre os requisitos
	- Codificar os casos de teste
		- Devido à frequente necessidade de repetição do teste cada vez que o software é modificado
	- O “tester” deve ser desde o mais crítico do sistema até ao mais independente (colegas, outro departamento, outra empresa)
	- Ser consciencioso relativamente a custos
	- Definir as saídas esperadas no teste com base nas especificações e não no código.

#### Estratégia de testes
- Estratégias ou abordagens de desenho de casos de teste
	- [[Caixa Branca]]
	- [[Caixa Preta]]

##### Caixa Preta Vs Caixa Branca
- A estratégia de ***“[[caixa preta]]”*** pode ser usada tanto para componentes de software grandes como pequenos
- Os testes de ***“[[caixa branca]]”*** são mais apropriados para testar componentes pequenos (pelo facto do detalhe requerido para o desenho do teste ser muito elevado)

