As [[métricas]] em engenharia de software são medidas quantitativas utilizadas para avaliar diversos aspetos do [[processo]] de desenvolvimento, [[qualidade]] e desempenho do software. Essas [[métricas]] fornecem dados objetivos que auxiliam na ***tomada de decisões***, ***gerenciamento de projetos***, ***avaliação de desempenho*** e ***melhoria contínua***.

É importante selecionar métricas relevantes para os objetivos específicos do projeto e do [[processo]] de desenvolvimento. O uso adequado de métricas pode contribuir para a identificação de áreas de melhoria, o monitoramento do progresso do projeto e a tomada de decisões informadas para aprimorar a qualidade e eficiência do desenvolvimento de software.
#### Importância da medição

- A medição da [[qualidade]] do software permite a determinação, previsão e melhoria da [[qualidade]] do [[produto]] e do [[processo]].
- Especificamente, as medições podem ajudar a **estimar os custos e os prazos** dos projetos de software, avaliar a **produtividade e antecipar as necessidades de manutenção**.
- As [[métricas]] de [[qualidade]] são essenciais para compreender a eficácia dos [[processo]]s de desenvolvimento de software e orientar a tomada de decisões.

#### Medição da qualidade do software
- A qualidade não pode ser determinada apenas pela aprovação nos testes; ela engloba:
	- **Qualidade do código**: estrutura, documentação, algoritmos.
	- **Avaliação não binária**: a qualidade existe num espetro, não apenas “qualidade vs. não qualidade”.

#### Métricas e medidas
- **Métrica**: Uma medida quantitativa dos atributos de um sistema de software.
- **Medida**: Uma indicação quantitativa de dimensões ou capacidades de atributos.
	Exemplo: Erros por linha de código (LOC) por homem-hora.

#### Classificação das métricas
- **Métricas de processo**: Resultados tangíveis das atividades de desenvolvimento de software.
- **Métricas de produto**: Métricas focadas no resultado do software em si.
- Principais áreas avaliadas:
	- Estado do projeto
	- Avaliação de riscos
	- Competências da equipa e capacidade de controlo da qualidade.

#### Tipos de medidas
- **Medidas diretas (internas)**: Custos, esforço, linhas de código (LOC), velocidade, utilização de memória.
- **Medidas indiretas (externas)**: Funcionalidade, [[qualidade]], complexidade, fiabilidade.

#### Categoria de Medição

| Categoria                      | Métricas                                   | Exemplos específicos                           |
| ------------------------------ | ------------------------------------------ | ---------------------------------------------- |
| Métricas de Gestão             | Tamanho (LOC, KLOC, Pontos de função)      | Duração da tarefa em horas, Esforço do projeto |
| Métricas de Qualidade Software | Densidade de defeitos, cobertura de testes | Defeitos por KLOC, Taxa de Remoção de Defeitos |
| Métricas de requisitos         | Solicitações de mudança e frequência       | Esforços para mudanças de requisitos           |
| Métricas de projeto            | Complexidade ciclomática, coesão           | Métricas de nível de classe como acoplamento   |
| Métricas de manutenção         | Tempo médio entre alterações               | Fiabilidade do sistema, tempo de inatividade   |

#### Factores de qualidade
- **Acoplamento**: Reflecte as relações de dependência entre módulos. É preferível um menor acoplamento.
- **Complexidade**: Medida através de várias métricas, incluindo as ***medidas de Halstead*** e a **complexidade de McCabe**.
###### Examples of Metrics in Context
- **Coupling Metrics**: RFC (Response for a Class), CBO (Coupling Between Objects).
- **Complexity Metrics**: Total operator and operand measures to assess code interpretability.

![[métricas 1.png]]

![[métricas 2.png]]

![[métricas 3.png]]

#### Métricas adicionais
- **Correção**: Defeitos por KLOC ou falhas por hora.
- **Manutenibilidade**: Tempo médio por alteração ou custo das correções.
- **Usabilidade**: Tempo de formação e competências necessárias para uma utilização eficiente.

#### Resumo e principais conclusões
- A medição da qualidade do software é multifacetada, envolvendo várias métricas internas e externas.
- Compreender as métricas do produto e do processo é crucial para a gestão eficaz de software e garantia de qualidade.
- A qualidade é um espectro que requer uma avaliação contínua para além dos meros critérios de aprovação/reprovação dos testes.