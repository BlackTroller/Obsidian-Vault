#### Definição de memória virtual

 - Espaço de memória passível de ser utilizada pelo conjunto de processos em execução, obtido pela gestão do ***espaço de endereçamento***. Espaço de endereçamento combina a utilização das memórias principal (RAM) e secundária (Discos).

- Gestão hierárquica das memórias principal (RAM) e secundária (Discos);
- Permite a utilização, como memória principal, de mais memória do que a fisicamente disponível;
- **Explora a diferença de velocidade** → RAM vs. discos.


- Memória virtual surge da necessidade de executar programas maiores do que a memória física disponível
- Conceito surgiu em 1961
- Funcionava de modo bastante simples
- Tamanho total do programa, dados e pilha poderia superar a memória física existente
- Desde de que se seleccione as partes, do programa, necessárias para a sua execução
- Carregando-as para memória e mantendo o resto em disco

#### Técnicas mais comuns de memória virtual

- Overlay (sobreposição)
- Paging (paginação)

#### Overlay

- Primeira solução encontrada
- Consiste na divisão do programa em segmentos de menor tamanho
- Cada um dos segmentos tem de ser capaz de ser contido em memória física
- Vários segmentos devem ter tamanhos muito aproximados
- Início da execução do programa, carrega-se o primeiro segmento para memória e é executado até ao fim
- Concluindo-se a execução de um segmento, este é substituído na sua totalidade pelo próximo *(overlay)*

- Permite a execução de programas de tamanho superior ao da memória existente
- Troca de overlay é da responsabilidade do sistema operativo
- Divisão do programa em overlays compete ao programador

#### Paging

- A mais adoptada pelos sistemas de memória virtual
- Assenta na capacidade de utilização de um conjunto limitado de endereços de memória, por parte dos programas
- Recorre para tal à **MMU** (Memory Managment Unit)
- Linha de código *assembly* leva o CPU a transferir para a zona de memória 1000 o conteúdo do registo BX
- Ao endereço de memória 1000, dá-se o nome de ***endereço virtual***
- Conjunto de endereços virtuais dá-se o nome de ***espaço de endereçamento virtual***
- Se não se usar memória virtual, então o endereço virtual vai ser utilizado diretamente, pelo barramento de memória, para aceder à informação
- Se se usar *Memória Virtual*, o endereço virtual será processado pelo **MMU**, obtendo-se assim o endereço físico correspondente, para enviar para o barramento de memória
- Espaço de endereçamento virtual é dividido em páginas *(pages)*
- Cada *page* corresponde a um segmento de memória física chamado de *page frame*
- *Pages* e *pages* frames têm obrigatoriamente o mesmo tamanho
- Tamanho varia entre 512b e 8KB\

##### Exemplo
![[paging.png]]

##### Paging - MMU

- ***Memory Managment Unit***
- Chip ou conjunto de chips
- Faz(em) parte do processador (CPU)
- Têm a responsabilidade de relacionar endereços de memória virtuais em endereços físicos
- Para um determinado endereço virtual, devolve um determinado endereço físico

![[paging - mmu.png]]

- Endereço virtual 8196 (0010000000000100)
- É transformado num endereço físico de 15 bits 110000000000100 (24580)
- Sendo este enviado de seguida para o barramento de memória

