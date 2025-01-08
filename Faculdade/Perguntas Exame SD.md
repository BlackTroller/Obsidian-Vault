#### Grupo 1

1. **Quais os objetivos de um Sistema Distribuído?**
- [ ] Disponibilização de recursos
- [ ] Escalabilidade
- [ ] Transparência 
- [x] Todas as anteriores
2. **Muitas vezes, no desenvolvimento de um Sistema Distribuído, é corretamente assumido:**
- [ ] Que a rede de comunicações é fiável.
- [ ] Que a rede de comunicações é fiável e homogénea
- [ ] Que a rede de comunicações é fiável, homogénea e segura
- [x] Nenhuma das anteriores
3. **Um Sistema Distribuído, para ser considerado Aberto, deve, pelo menos, ser independente:**
- [ ] do Hardware
- [ ] da Plataforma
- [ ] do Hardware e da Plataforma
- [x] do Hardware, da Plataforma, e das Linguagens
4. **Um Sistema Distribuído Aberto:**
- [x] Apresenta uma capacidade de extensão do mesmo através da adição de novos componentes
- [ ] Não é importante que sejam conhecidas as interfaces dos novos componentes
- [ ] Deve usar protocolos e formatos proprietários
- [ ] Nenhuma das anteriores
5. **Context switching é o ato:**
- [ ] de trocar de um processo para uma thread 
- [x] de guardar o contexto do processo em curso 
- [ ] de trocar de uma thread para um processo
- [ ] Nenhuma das anteriores
6. **Uma thread permite:**
- [ ] Partilhar variáveis
- [ ] Melhorias de performance 
- [ ] Esconder latências 
- [x] Todas as anteriores
7. **O fornecimento contínuo de um serviço pode ser classificado como:**
- [x] Disponível
- [ ] Fiável
8. **O tipo de comunicação que armazena as mensagens é chamada de comunicação:**
- [x] Persistente
- [ ] Transiente
9. **O modelo de avarias apresenta diferentes tipos:**
- [x] Avarias por omissão
- [ ] Avarias controladas
- [ ] Avarias sem tempo
- [ ] Todas as anteriores
10. **A computação distribuída pode ser definida como:**
- [ ] Um conjunto de unidades que executam concorrentemente em elementos de computação diferentes 
- [ ] Um conjunto de diferentes processadores na mesma máquina 
- [ ] Um conjunto de diferentes processadores em diferentes máquinas 
- [x] Todas as anteriores
##### Verdadeiro e Falso
11. **DNS é um Sistema Distribuído que, embora centralizado, escala com facilidade.**
- [x] Verdadeiro
- [ ] Falso
12. **Em qualquer canal de comunicação deve ser garantido autenticação, integridade e confidencialidade.**
- [x] Verdadeiro
- [ ] Falso
13. **Numa crash failure de um componente, este comporta-se de forma correta antes e depois do bloqueio.**
- [ ] Verdadeiro
- [x] Falso
14. **É fácil de distinguir um componente crashado de um componente, simplesmente, mais lento.**
- [ ] Verdadeiro
- [x] Falso
15. **Multitasking é uma técnica que os SO usam para criar a ilusão de que múltiplos processos estão a correr em simultâneo.**
- [x] Verdadeiro
- [ ] Falso
16. **Uma vez criado, um socket, somente serve para receber ou para enviar mensagens.**
- [ ] Verdadeiro
- [x] Falso
17. **A utilização do protocolo UDP em aplicações onde são aceitáveis avarias de omissão não é possível.**
- [ ] Verdadeiro
- [x] Falso
18. **Requisitos para confiabilidade podem ser: indisponibilidade (unavailability), confiabilidade (reliability), segurança (safety), capacidade de manutenção (maintainability).**
- [ ] Verdadeiro
- [x] Falso
19. **Deve-se sempre verificar o estado de um certificado antes de confiar na informação, dado que ele pode estar expirado ou ter sido revogado.**
- [x] Verdadeiro
- [ ] Falso
20. **O UDP (User Datagram Protocol) é um protocolo sem conexão em que a comunicação por “streams”.**
- [ ] Verdadeiro
- [x] Falso
#### Grupo 2
1. **Distinga, por palavras suas, Sistema Distribuído de Computação Distribuída:**
Sistema distribuído é um conjunto de computadores ligados em rede com software que permita a partilha de recursos e a coordenação de atividades enquanto que computação distribuída é distribuída em várias unidades que executam concorrentemente em diferentes elementos de computação. Pode ser diferentes processadores em diferentes máquinas, diferentes processadores na mesma máquina ou diferentes cores no mesmo processador.

2. **Explique por palavras suas, porque é que a mudança de contexto entre “Threads” de um mesmo processo é menos “pesada” que a mudança de contexto entre “Threads” de processos distintos.**
porque threads do mesmo processo já tem facilidade de partilhar recursos/dados entre si enquanto que threads de processos diferentes pode demorar mais tempo a conseguir obter os recursos porque tem outras threads, processos ou ambientes de execução diferentes antes e que possam atrasar a obtenção dos mesmos.

3. **Porque é que, em streaming de vídeo ou áudio, se usa muitas vezes UDP em detrimento de TCP? Explique a principal diferença que contribui para esta escolha.**
O Protocolo UDP é preferido em streaming de video e áudio porque prioriza a baixa latência e a transmissão mesmo que ocasionalmente ocorram a perca de pacotes. Diferente, do protocolo TCP que que garante a entrega de pacotes através de retransmissões o UDP permite o streaming continuo, ignorando a perca de pacotes para não haver atrasos na transmissão.