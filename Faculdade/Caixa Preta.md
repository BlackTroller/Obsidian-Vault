#### Testes de Caixa Preta

- Abordagem/estratégia também conhecida como ***“testes funcionais”***
- **Avaliam o comportamento externo do componente de software, sem se considerar o comportamento interno do mesmo** 
- ***Apenas são consideradas as entradas e saídas*** como uma base para desenho dos casos de teste 
- **Objetivo**: assegurar que os requisitos do software e as especificações foram atendidos, ou seja, valida se o que foi especificado foi implementado corretamente
- É executado considerando como base **os requisitos e as funcionalidades do software** 
- Quanto mais entradas são fornecidas, mais rico será o teste. Numa situação ideal todas as entradas possíveis seriam testadas, mas na ampla maioria dos casos isso é impossível

- O *“Tester”* (engenheiro de software) pode derivar um conjunto de condições de entrada que exercitem praticamente todos os requisitos funcionais para um programa 
- O *“Tester”* fornece os inputs (entradas) , os testes são executados e é verificado se os resultados obtidos são “equivalentes” aos previamente especificados 
- Os testes de caixa preta **procuram descobrir erros** nas seguintes categorias:
	- funções incorretas ou ausentes
	- erros de interface 
	- erros nas estruturas de dados ou no acesso a base de dados externas 
	- erros de inicialização e de término.

- Tipicamente, são projetados para responder às seguintes questões:
	- Como é testada a **validade funcional de um sistema** 
	- **Que classes** (e.g. conjunto de valores) de entrada poderão constituir bons casos de teste? 
	- O sistema é particularmente **sensível a determinados valores de entrada**? 
	- Como estão **isoladas** as fronteiras de uma determinada classe de dados? 
	- Quais os **índices de dados e volumes de dados** que o sistema pode tolerar? 
	- Que efeito poderão ter certas combinações específicas de dados sobre a operação do sistema?

- Numa abordagem baseada em testes de [[caixa preta]], para testar uma determinada operação, o *“tester”* deve obter casos de teste suficientes para verificar que:
	- para cada valor aceite ***(escolhido)*** como valor de entrada ***(input)***, um valor apropriado é retornado ***(output)*** pela operação.
	- para cada valor não aceite ***(escolhido)*** como valor de entrada ***(input)***, apenas um valor apropriado é retornado ***(output)*** pela operação 
	- para cada **estado de entrada válido** ocorre um **estado de saída apropriado **
	- para cada **estado de entrada inválido**, ocorre um **estado de saída apropriado**

#### Técnicas
- Alguns métodos (técnicas) de caixa preta:
	- Equivalence Class partitioning (Partição em classes de equivalência) 
	- Boundary Value Analysis (Análise de valor limite) 
	- Cause-and-Effect Graphing (Técnicas de Grafos de causa-efeito) 
	- Random testing 
	- Error Guessing
	- State Transition Testing

##### Equivalence Class Partitioning (ECP)
- Técnica destinada a ***reduzir o número de testes necessários*** 
- Técnica que **divide o domínio de entrada (ou saída) em classes de dados** em que os ***casos de teste podem ser derivados***
- Para cada operação, o *“tester”* deve identificar as **classes de equivalência** dos argumentos e os **estados dos objetos** 
- Uma **classe de equivalência**: um conjunto de valores de acordo com os quais o objeto se deve comportar 
- Por exemplo, um Conjunto contém três classes de equivalência: vazio, algum elemento e cheio
- Deve-se considerar classes de valores válidos e valores inválido
	- Exemplo para ***sqrt(x): x<0 (inválido), x>=0 (válido)***
###### ECP - Exemplo
- **Testar uma função que calcula o valor absoluto de um inteiro X**
Classes de equivalência:
![[ECPExemplo.PNG]]

##### Boundary Value Analysis (BVA)
- Técnica **focada nos limites do domínio de entrada (ou saída)** e imediatamente acima e abaixo (além de ou em vez de valores intermédios) 
- Testar também valores especiais (null, 0, etc.) 
- Baseada na observação de que bugs ocorrem frequentemente em valores fronteira:
	- Problemas com índices de arrays, decisões, overow, etc.
	- Se o sistema se comportar bem nos casos fronteira então provavelmente comportar-se-á bem em valores intermédios.
###### BVA - Boas Práticas
- Para um dado domínio de valores:
	- Se as condições de entrada especificarem um intervalo entre a e b, os casos de testes deverão incluir a e b, bem como valores acima e abaixo de a e b.
	- Se a condição de entrada especificar um número de valores, os casos de teste deverão contemplar o valor máximo e mínimo desses valores, bem como valores abaixo e acima do valor mínimo e do valor máximo.
	- Se as estruturas de dados internas do programa tiverem limites (e.g. limite de tamanho), o “tester” deverá certificar-se de que testa os limites.
###### BVA - Partições segundo as condições
- **P1 - Entradas de acordo com as pré-condições (válida)**
	- array com um valor (valor limite) 
	- array com mais de um valor (de diferente tamanho de caso de teste para caso de teste)
- **P2 - Entradas em que a pré-condição não é assegurada (inválida)**
	- array com tamanho zero
- **P3 - Entradas em que o elemento chave é membro do array**
	- alternar a primeira, a última e a posição do meio em diferentes casos de teste.
- **P4 - Entradas em que o elemento chave não é membro do array**

	