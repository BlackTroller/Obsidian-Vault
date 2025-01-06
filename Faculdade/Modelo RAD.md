E se para além **da necessidade de lidar com a incerteza** associada a um projeto, ***O tempo é um fator crítico?***
- como **rapidamente** *compreender os detalhes dos requisitos* e automatizar a sua codificação progressiva?

![[RAD.png]]

- **[[Processo]] iterativo de desenvolvimento de software**
- Versão *"high-speed"* do [[modelo em cascata]], usando uma abordagem ao desenvolvimento baseada em componentes.
- Ideia básica:
	- desenvolver e entregar um sistema como elevados índices de qualidade ao mais baixo custo possível
- Divide o problema em problemas mais simples o que lhe confere uma menor resistência à mudança
- Pode fazer uso de protótipos fazendo bastante uso de [[ferramenta]]s GUI e CASE (computer aided Software Enginnering) e Database Management Systems (DBMS) e ainda linguagens de 4ª geração, geradores de código e técnicas orientadas por objetos.

###### Criar um sistema funcional num curto espaço de tempo (60 a 90 dias)
- Aplicável se: 
	- Os requisitos são bem entendidos
	- o âmbito do projeto é restrito

###### Modelo de Negócio
- Que **informação** suporta o **processo de negócio?**
- Que **informação** é gerada e **quem a gera?**
- Para onde flui a **informação** e **quem a processa?**

###### Modelo de dados
- **Fluxo de informação** => "objetos de dados" de suporte ao negócio
###### Modelo de processo
- **Descrição do processo** <=> adicionar; modificar; remover; ou recuperar a informação de um objeto

##### Rad Implica:
- Reusar componentes - quando possível
- Criar componentes reutilizáveis - quando necessário
- os pontos anteriores implica o uso de técnicas denominadas da 4ª geração([[ferramenta]]s automáticas)
- tempo significa €€€€€€€€€€€€€€, ou seja com isto queremos dizer que para fazer no menor possível precisamos é precisar gastar bastante dinheiro

###### RAD adequa-se a todo o tipo de projetos/aplicações?
***Não!!***
- Se **não for possível modularizar** o sistema, então não
- Se **a performance** é uma questão muito pertinente, então cuidado
- quando **os riscos técnicos são elevados**, então não
