
- É geralmente descrito **como um grupo de procedimentos realizados para avaliar algum aspeto ou parte de software**
	- Pode ser descrito:
		- como um [[processo]] usado para revelar defeitos no software e para estabelecer que o software atingiu um grau especificado de [[qualidade]] relativamente aos atributos selecionados.

- Cobrem as atividades de validação e verificação, e incluem no domínio de *testing* tudo o que se segue:
 ![[testing.PNG]]
 - Estas definições também descrevem ***“testing”*** com um [[processo]] com um propósito duplo
	 - que revele defeitos
	 - e que é usado para avaliar atributos de [[qualidade]] de software, tais como segurança, usabilidade e exatidão

#### Teste vs Debug

![[testevsdebug.PNG]]

#### Inspeções de código e testes

* **SW Inspections**
	* Verificação estática. Focada numa determinada representação estática do sistema com o intuito de "descobrir" problemas.
* **SW Testing**
	* Verificação dinâmica. avalia o comportamento observável de um [[produto]] de software

![[insCod.PNG]]


- examinação (estática) da fonte*(Não necessariamente código fonte. Pode ser a representação fonte ou base dos requisitos.) com o intuito de descobrir problemas 
- não requer a execução do sistema 
- esta observação/examinação pode ser aplicada a **requisitos, design, dados de configuração, dados de teste, etc...**
- *na realidade é uma boa técnica para descoberta de erros.*


- Durante a execução há erros que “encobrem” outros erros 
- Não há a necessidade e/ou preocupação com interações 
- Versões incompletas podem ser inspecionadas 
- Aquando da inspeção podemos considerar outros atributos da qualidade como por exemplo: conformidade com standards, padrões, portabilidade etc...
- Contudo, as inspeções não conseguem avaliar a conformidade com os requisitos reais do cliente nem questões relacionadas com usabilidade e performance 
- **SW Inspections** e **Software Testing** são complementares


