## Sistemas de Informação em Engenharia Informática

### Conceitos e Fundamentos

- **Orientação Funcional**: Estrutura organizacional focada nas funções específicas.
- **Orientação a Processos**: Estrutura organizacional que prioriza os processos de negócio sobre funções.

### Modelo de Negócio

- **Alinhamento**: Conectar o modelo de negócio aos mapas de processos é essencial para garantir eficiência.

### Métodos e Técnicas de Análise

- **Identificação de Processos**: Registro e análise de todos os processos envolvidos na organização.
- **Modelos AS-IS e TO-BE**:
    - **AS-IS**: Descrição do estado atual dos processos.
    - **TO-BE**: Visão do estado futuro desejado dos processos.
- **Documentação Detalhada**: Criação de documentação que abrange todos os aspectos dos processos.

### Matriz SIPOC

- **SIPOC**: Supplier, Input, Process, Output, Customer. Uma ferramenta para mapear e visualizar processos rapidamente.

### BPMN (Business Process Model and Notation)

- **Definição**: Um padrão gráfico para modelagem de processos, promovendo clareza e compreensão entre stakeholders.
- **Elementos Gráficos**:
    - **Flow Objects**: Representação das atividades no processo (Eventos, Atividades, Decisores).
    - **Connecting Objects**: Demonstra as conexões e interdependências entre atividades.
    - **Swimlanes**: Representa diferentes departamentos ou grupos que intervêm no processo.
    - **Artifacts**: Detalhes adicionais que complementam o diagrama, como grupos e notas.

### Elementos de Fluxo em BPMN

|**Elemento**|**Descrição**|**Tipo**|
|---|---|---|
|**Evento**|Algo que ocorre durante o processo (Start, Intermediate, End)|Exemplo: Início de um processo|
|**Atividade**|Trabalho realizado (Atômica ou Não-atômica)|Exemplo: Confirmar pedido|
|**Decisor**|Controla a divergência e convergência no fluxo|Exemplos: XOR, AND, OR Gateways|

### Exemplos e Aplicações

- **Exemplo 1: Processo de Pedido a Dinheiro**:
    
    - **Fluxo**: Receber pedido → Verificar estoque → Emitir fatura → Enviar mercadoria.
    
   ```plaintext
    Start Event --> Check Stock --> Confirm Order --> Send Invoice --> Ship Goods --> End Event
    ```
    
- **Práticas Recomendadas**:
    
    - Nomear eventos e tarefas claramente.
    - Evitar anti-padrões que comprometam a clareza, como:
        - Falta de eventos de início e fim.
        - Atividades não conectadas corretamente.

### Anti-padrões

- **Erros a Evitar**:
    - Falta de um evento de início e fim.
    - Atividades desconectadas em uma pool.
    - Uso incorreto de fluxo de sequência e mensagens.

### Recursos Adicionais

- Documentos e exemplos disponíveis nos sites BPMN e Camunda para aprofundamento nos conceitos e práticas.

### Summary & Key Takeaways

- **BPMN** é essencial para representar graficamente os processos de negócio, facilitando a compreensão e comunicação.
- Implementar práticas corretas e evitar anti-padrões garantem a eficiência na modelação de processos.
- O alinhamento do modelo de negócio aos processos é crucial para a eficácia organizacional.

###### Notação do BPMN
![[BPMN 1.png]]

**Elementos Flow**
![[BPMN 2.png]]

**XOR**
![[BPMN 3.png]]

**And**
![[BPMN 4.png]]

**OR**
![[BPMN 5.png]]