- A Garantia da [[Qualidade]] do Software é “um **conjunto de ações planeadas** e sistemáticas, necessárias **para assegurar** a **[[Qualidade]]** no **Software** ” [Schulmeyer, 1987]

-  A Garantia da qualidade do software é composta por várias tarefas associada a dois grupos diferentes:
	- **Engenheiros** de **Software** , que executam o trabalho técnico
	- A **Equipa** de **SQA** (Software Quality Assurance), responsável pelo planeamento, acompanhamento, registo de informação, análise e relatórios sobre a Garantia da [[Qualidade]]

##### SQA Plan
- O **plano SQA** define **os meios que irão ser usados** para **garantir que o software desenvolvido** no **âmbito de um determinado [[produto]] de software satisfaz os requisitos do utilizador** e que respeita amplamente as restrições do projeto a um nível de qualidade alto.
- Como?
	- primeiro é necessário definir e perceber claramente o “quality target”.
	- deve ser considerado: a gestão, o desenvolvimento e os planos de manutenção para o software.
	- • O **standard IEEE730-98**, define os detalhes do “Software Quality Assurance Plan”-

- O que contem o **SQA Plan**
- Identifica:
	- **documentos, standards, práticas e convenções** que regem o projeto de modo **a controlar e monitorar** para garantir a adequação e conformidade;
	- **medidas, técnicas (estatísticas) e procedimento para reportar problemas e ações corretivas, recursos ([[ferramenta]]s, técnicas e [[metodologia]]s), formação** e indicações de como criar documentação específica

##### SQA - Other Activities
- contempla também:
	- outras atividades para garantia de [[qualidade]] de software que estejam no **SQA Plan**, nomeadamente:
	- procurement of supplier software (aquisição de software) ou
	- commercial off-the-shelf software (COTS), e
	- serviços pós-venda;
- pode ainda conter:
	- critérios de aceitação e ainda atividades de report e gestão consideradas críticas para a [[qualidade]] de software

##### Categories of SQA Work
- Um trabalho típico de garantia da **[[qualidade]]** de software abrange **6 dimensões**:
	- [[método]]s e [[ferramenta]]s de construção
	- revisões formais
	- estratégia de teste *
	- **controlo de documentação** e histórico de mudanças
	- procedimentos para garantir a adequação aos padrões de desenvolvimento
	- mecanismos de **medição e análise** *

* No caso dos testes
	* O erro começa em desvalorizar o [[processo]] de testes
	* Existem [[ferramenta]]s de teste que permitem a automação dos testes, no entanto, deve-se usar a mais adequada e ter um [[processo]] de testes claro e definido
	* Efetuar planeamento dos testes
	* O custo do [[processo]] e de uma [[ferramenta]] de testes será diluído no tempo e nos “bugs” eliminados previamente.
* No caso dos **mecanismos de medição**
	* o problema é a indefinição do que se deve medir
	* o erro é desenvolver o software de **forma reativa e não de forma pró-ativa**, corrige- se aquilo que é reclamado ou questionado, se ninguém analisou não tem erros...

##### Software Quality - direct and indirect factors
- Existem dois grandes grupos que afetam a [[qualidade]] de software
	- o que pode ser **medido de forma direta**
		- ex: número de erros , linhas de código (para cada situação deve haver um processo de medição)
	- o que pode ser **medido de forma indireta**
		- ex: usabilidade, etc

![[SQA.PNG]]

##### SQA - [[Testing]]
- Estratégia mais popular de **gestão de risco**
- Usados para verificar o encontro dos requisitos com o [[produto]]
- Nem todos os defeitos são descobertos durante os testes
- Testes de software incluem atividades de verificação e validação das atividades do [[processo]] de desenvolvimento

##### SQA - Quality Control
- [[Processo]]s e [[método]]s usados para monitorar o trabalho e os requisitos envolvidos
- É focado nas **revisões e remoção de defeitos** antes da entrega do produto
- Consiste em checks do [[produto]] bem definidos que sejam especificados dentro do plano de garantia de [[qualidade]]
- Revisões de especificação, inspeções de código e documentos, e checks de entrega ao utilizador

##### SQA - Software Configuration Management
- Refere-se a **“etiquetar”, rastear e controlar as mudanças** nos elementos do software ou do sistema
- Controla a **evolução do sistema pela gestão das versões dos componentes de software** e seus relacionamentos
- O objetivo é **identificar todos os componentes do software interrelacionados e controlar a sua evolução através das fases do ciclo de vida do software**
- Controla o código e documentos associados de tal maneira que o código final e a sua descrição sejam consistentes e representem aqueles itens que eventualmente foram revistos e testados

- **Gestão de configuração de SW** (engloba fundamentalmente):
	- component identification;
	- version control;
	- config. building;
	- change control;

![[SQAConfig.PNG]]

***Conjunto de atividades desenvolvidas para gerir a mudança ao longo do ciclo de vida de desenvolvimento de software***

- **Necessidade**
	- Porque trabalho em equipa
	- Porque há diferentes versões de software; 
	- Porque há várias *releases* para o cliente; 
	- Porque o SW muda rápidamente
- **Logo**
	- Há a necessidade de gerir o [[processo]] e garantir *“agilidade”* no mesmo!
- **Tarefas**
	- Identificar *work products (WP) susceptíveis mudança; 
	- Estabelecer relações entre eles (os WP);
	- Estabelecer mecanismos de gestão das diferentes versões desses WP **(Gestão de Versões)**
	- Estabelecer o processo de assemblagem de todos os componentes **(Building)**
	- Controlar as alterações **(Gestão de Alterações)**
	- Auditar e reportar as alterações **(Inspeções)**
	- Preparar o software para entrega **(Release Management)**

##### Processo SCM
**Dos Requisitos...**

![[SQASCM.PNG]]

##### SCM vs DevOps
- Ambos se referem aos mesmos princípios:
	- **DevOps** é mais recente e menos formal. Emergiu do vocabulários Agile
	- **SCM** é um conceito bem definido no âmbito da [[engenharia de software]]

![[SCMVSDEVOPS.PNG]]

