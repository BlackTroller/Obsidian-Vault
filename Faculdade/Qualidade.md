
# Qualidade de software 

Como assegurar a qualidade do __[[produto]]__ de software e do __[[processo]]__ de desenvolvimento de software?

### Sobre qualidade de software... 

**O quê?**
**Como?**
**Com Quem?**
**Apoiado por que [[ferramenta]]s?**
**Em que circunstâncias?**

**...podemos produzir software de alta [[qualidade]]?**

![[rumo à qualidade do software.png#right|600]]

### Guia para a qualidade do software

Para começar a modelar um software, que apresente uma solução para o problema e garantir a sua [[qualidade]], normalmente, desenvolve-se um ***S.R.S*** **(System Requirements Specifications)**.

Após, aplica-se [[modelo]]s ([[método]]s) para se conseguir desenvolver uma solução, uniformizada e sistematizada. Deve-se seguir as normas, apesar de, para alguns engenheiros, técnicos e designers, ser um “inibidor da criatividade“, assim garante-se que os software irá ter [[qualidade]]. 
Só após, existir um [[modelo]] de uma solução, é feita a escolha, de uma/várias [[ferramenta]](s), mais indicada(s), para construir o nosso programa.

Sendo assim um software que tenha [[qualidade]] elevada é pós-ativo no [[processo]], preventivo nos problemas e defeitos e cumpre todos os requisitos (funcionais e não funcionais) do S.R.S.

Podemos concluir que, para garantir a [[qualidade]] de software, deve-se garantir a qualidade de [[produto]] e a qualidade de [[processo]]. Não há garantia quanto à definição da [[qualidade]] de software.

- o 1º passo para garantirmos  ***qualidade do software*** é necessário definirmos bem o nosso ***objetivo*** que o nosso software consiga resolver.

![[roadmap 1.png]]

- o 2º passo para garantirmos ***qualidade do software*** é necessário perceber as ***perspectivas*** em que o nosso software vai ser utilizado.

![[roadmap 2.png]]


![[roadmap 3.png]]

- No 3º passo para garantirmos ***qualidade de software*** é necessário seguir os ***standards*** e as ***Práticas estratégicas*** como teste de software e como definir a [[metodologia]] para o software. 

![[roadmap 4.png]]

- lorem ipsum

![[roadmap 5.png]]

- Ou seja [[qualidade]] de software implica Qualidade do [[Processo]] + Qualidade do [[Produto]] e isso são os nosso fundamentos básicos como ***What?*** ([[Processo]]) , ***Lógica*** ([[Modelo]]) e ***How?*** ([[Método]]/[[Metodologia]]).

![[roadmap 6.png]]

O grande objetivo de uniformizar, sistematizar e automatizar o problema (aplicar os conceitos fundamentais de engenharia) é garantir a [[qualidade]] de software. É possível abordar esta temática através de uma perspectiva do [[produto]] ou do [[processo]] (**normas ISO/IEC 9126 , TickIT + ISO 900 + CMMI** respectivamente) (Ambas as perspectivas usam o ***SQA***, **Software Quality Assurance**, que consiste em verificar o software, rever o software e a sua validação).

### Perspectiva (vistas) sobre a qualidade de software

- A [[Qualidade]] do [[Processo]] e a [[Qualidade]] do [[Produto]] estão interligados. Não devemos dissociar o processo do produto.
- No entanto, o foco poderá ser maior numa ou noutra componente.

A [[qualidade]] pode ser melhorada através de um [[processo]] de revisão, avaliação e de melhorias iterativo e continuo que necessita de um sistema de controlo de versões (GIT) (ciclo de vida do software) e prevenção de erros mais a sua remoção. 

- Os standards que regem a [[qualidade]] do [[processo]] são: 
	* TickIT; 
	* ISO 9001-00; 
	* CMMI. 

O standard da **[[qualidade]] de [[produto]]** é a ***ISO 9126-01***. A [[qualidade]] total ou a ***T.Q.M.*** (**total quality management**), depende: 
* da **Mão de obra** (o quanto ***qualificada*** é), 
* das **Melhorias** constantes (nos ***[[processo]]s***); 
* e no **Foco** no cliente. 
Que resulta em: 
* ***[[Métricas]]***; 
* ***[[Modelo]]s***; 
* ***Medições***; 
* ***Análises***.
O ***total quality management*** possui vários níveis: 
1. **Inspeção**:  Consiste em verificar o ***S.R.S.*** . 
2. **Controlo de qualidade**: São o conjunto de inspeções, revisões e testes utilizados durante o ciclo de desenvolvimento para assegurar que cada [[produto]] cumpre os requisitos previstos (medições e feedbacks). 
3. **Garantia de [[qualidade]]**; 
4. **[[Qualidade]] Total**

#### Fundamentos de Qualidade de Software

![[SWQualityFundamentals.jpg]]


A qualidade de software é avaliada com base em normas específicas e **requisitos**, que podem ser explícitos ou implícitos, definindo as características necessárias para medir o desempenho e a fiabilidade do software. A ***norma ISO9126-01*** é um padrão que orienta a avaliação da **qualidade do produto**, enquanto ***normas como TickIT***, ***CMMI*** e ***ISO9001-00*** estão focadas na **qualidade do processo**.

A **qualidade do produto** é analisada em três áreas principais. A *revisão do produto* foca-se na testabilidade, flexibilidade, manutenibilidade e integridade. A *operação do produto* considera a eficiência, fiabilidade, correção e usabilidade. Por fim, a *transição do produto* aborda a reutilização, interoperabilidade e portabilidade. Estes fatores são fundamentais para garantir que o software atende aos **requisitos funcionais** e de **desempenho** esperados.

![[qualidade do produto.PNG]]

Por outro lado, a **qualidade do processo** desempenha um papel crucial na garantia de que as *práticas* utilizadas no desenvolvimento e manutenção do software estão alinhadas com padrões consistentes, contribuindo assim para a melhoria contínua do produto final. Este **modelo** é uma abordagem abrangente para compreender e **otimizar** a **qualidade** no desenvolvimento de software.

![[ISO9126.PNG]]

* **A versão ISO/IEC 9126 é substuída por ISO/IEC 25010:2011** acrescentando o fator “compatability” e “performance”, redistribuindo algumas das sub-categorias

![[NEWISO.PNG]]


#### Requisitos de Qualidade
***Apesar das varias definições, é consensual que:***

- Os [[requisitos de software]] definem as características de [[qualidade]] do software e influenciam os [[método]]s cálculo e critérios de aceitação para avaliar essas características.

![[SWQualitySwebok.PNG]]

#### Ética e Qualidade de Software

The **IEEE Computer Society and the ACM (IEEE99)** desenvolveram um código de ética de práticas profissionais baseadas em *8 princípios que assistem os engenheiros de software a reforçar atitudes relacionadas com a qualidade* e com a independência do seu trabalho.

![[IEEENorms.PNG]]

* addictive design; 
* corporate ownership of personal data; 
* algorithmic bias; 
 * Bias might be as bad as a virus. 
 * ***Example: not to include Black people's voices in training AI speech recognion algorithms, under the belief that fewer Black people would use the app.***
* Weak cyber security and personally identifiable information (PII) protection; 
 * ***Developers only address security after code*** 
* overemphasis on features. ***Some believe that capabilities in software releases are more important than the effects they could have.***

#### Qualidade e Custos da Qualidade

- A visão de quem usa:
	**"Um Produto ou Serviço que faz o que o utilizador precisa"**

* *Os Atributos de qualidade são (ou derivam ser) descritos na especificação de requisitos*

 - Exemplos:
	 - **Usabilidade** - Relativa facilidade de comunicação do utilizador com a aplicação
	 - **Portabilidade** - Capacidade de o sistema trabalhar sob diferentes tipos de arquitetura
	 - **Reusabilidade** na construção 

- O custo da Qualidade de Software pode ser dividido em ($):
	- Custos de **prevenção**
	- Custos de **avaliação**
	- Custos de **falhas internas**, e
	- Custos de **falhas externas.**

###### O que isso nos garante?
- **A Gestão da Qualidade diminui os Custos.**
- **Prevenir Custos** - conjunto de ações tomadas para prevenir os defeitos antes que eles apareçam
- **Custos de inspeção** - Consistem em medir, avaliar e auditar produtos ou serviços para avaliar a conformidade com os padrões e especificações
- **Custos de falhas internas** - consistem em *corrigir defeitos dos produtos* antes de serem "entregues"
- **Custos de falhas externas** - consistem nos *defeitos descobertos depois do produtos ser entregue*
	- Quantas mais falhas externas forem encontradas, mais desastroso será para a reputação da organização.

#### Gestão de Qualidade

* Algumas medidas de qualidade incluem:
	* *Estruturação de um [[processo]] de desenvolvimento com [[método]]s, técnicas e ferramentas*
* Programa de gestão de qualidade inclui:
	* **Documentação** de padrões de código
	* **[[Método]]s**
	* **Ferramentas**
	* Procedimento de recuperação de dados 
	* **Gestão de configurações**
	* Documentação dos defeitos encontrados
	* **Rastreabilidade**

##### Comparação Fatores Qualidade

![[CompareFatoresQualidade.PNG]]

##### Qualidade do Produto

A qualidade do produto de software pode ser melhorada **através de um [[processo]] iterativo de melhoria contínua** que inclui:

- **Controlo da Gestão**;
- **Coordenação** e
- **feedback** dos vários processos concorrentes, nomeadamente:
	- o [[processo]] do ciclo de vida do software
	- o [[processo]] de deteção de erros/defeitos, prevenção e remoção
	- o [[processo]] de melhoria da [[qualidade]]

##### Qualidade Total

![[TQM.PNG]]

##### TQM - Níveis de Qualidade

1. **Inspeção** - Verificação pelo respeito das especificações internas em vigor
2. **Controlo de Qualidade** - conjunto de *inspeções, revisões* e *testes* utilizados durante o ciclo de desenvolvimento para assegurar que cada produto de trabalho cumpre requisitos previstos. Baseia-se na medição e "feedback"
3. **Garantia de Qualidade** - Baseada na ***prevenção do problema*** e não na sua deteçao. Consiste em auditorias (avaliações periódicas) e divulgação dessa informação à gestão
4. **Qualidade Total**
	* A qualidade é definida pelo cliente (ou junto com o cliente)
	* A qualidade representa uma **vantagem competitiva**
	* A qualidade é **parte integrante do processo de planeamento estratégico**
	* A qualidade **requer o comprometimento** de todos os recursos humanos da empresa

###### Qualidade de software - disciplina

É uma área de conhecimento da Engenharia de Software que tem como objetivo garantir a qualidade do software através da ***definição e normalização de processos*** de desenvolvimento

###### Qualidade de software - foco

- A definição anterior aponta 3 pontos importantes: 
	- **Os requisitos do software** são a base a partir da qual a qualidade é medida. Falta de conformidade com os requisitos é falta de qualidade. 
	- **Normas especificadas** definem um conjunto de critérios para o desenvolvimento que orientam o modo como o software é desenvolvido. Se os critérios não são seguidos a falta de qualidade resultará, muito provavelmente. Normas e critérios relacionados com a cultura empresarial. 
	- Há um conjunto de ***requisitos implícitos*** que nunca são mencionados (p.ex., facilidade de manutenção). Se o software falha a conformidade com estes requisitos implícitos, a qualidade é “suspeita”.

#### Software Quality management

- ***Define***:
	- **Processos**
	- **donos dos processos e os requisitos desses processos**
	- **medida dos processos** e os seus outputs e canais de feedback
- Consiste em várias atividades e ***envolve***: a **definição** do produto no que diz respeito às suas **características de qualidade**; **Planear todo o processo** para alcançar o referido produto.

- Alguns dos processos especificados pela *Gestão da Qualidade do Software* encontram-se definidos no *Standard (IEEE12207.0-96)*, nomeadamente:
- 