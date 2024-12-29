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
- •Um **erro** é um engano, uma ideia errada/equívoco, ou interpretação errada/má compreensão por parte de um “desenvolvedor” de software
- Na categoria de “desenvolvedor” incluímos engenheiros de software, programadores, analistas e os testers.
	- Exemplo: um “desenvolvedor” entender mal a notação de desenho, um programador digitar o nome de uma variável incorretamente

