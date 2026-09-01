# Relatório de Análise de Hardware

## 1. Situação atual

A empresa apresenta problemas significativos de lentidão nos computadores e na rede, afetando a produtividade dos funcionários, a eficiência das operações e o desempenho dos sistemas utilizados.

Como não foram fornecidas especificações detalhadas dos computadores atualmente utilizados, a análise considera uma configuração empresarial de referência e propõe componentes com foco em desempenho, confiabilidade e custo-benefício.

## 2. Problemas identificados

Os principais fatores que podem contribuir para a lentidão são:

* quantidade insuficiente de memória RAM;
* utilização de armazenamento baseado em HDD;
* processadores de baixo desempenho ou defasados;
* infraestrutura de rede limitada;
* equipamentos de rede sem capacidade adequada para o volume de tráfego;
* ausência de recursos gráficos suficientes para atividades que demandem processamento visual.

## 3. Componentes recomendados

### 3.1 Memória RAM

Recomenda-se a utilização de **16 GB de RAM** nos computadores destinados às atividades administrativas e operacionais.

Essa capacidade permite executar simultaneamente o sistema corporativo, navegador, ferramentas de comunicação e demais aplicações utilizadas no ambiente empresarial com maior margem de desempenho.

### 3.2 Armazenamento

Recomenda-se substituir unidades HDD por **SSD**.

O SSD proporciona menor tempo de acesso aos dados e melhora significativamente operações como inicialização do sistema operacional, abertura de aplicações e leitura e gravação de arquivos.

Para computadores corporativos de uso geral, recomenda-se inicialmente um SSD de **480 GB ou 500 GB**, dependendo da disponibilidade e do custo.

### 3.3 Processador

Recomenda-se a utilização de um **processador intermediário atual**, com múltiplos núcleos e threads.

Esse perfil atende às atividades administrativas, sistemas corporativos, navegação web, videoconferências e aplicações de produtividade sem elevar desnecessariamente o custo do equipamento.

### 3.4 Placa de vídeo

Para computadores destinados a atividades administrativas, não é necessária uma placa de vídeo dedicada.

A utilização de **GPU integrada ao processador** é suficiente para aplicações de escritório, sistemas corporativos, navegação web e reprodução de conteúdo multimídia.

Uma GPU dedicada deve ser considerada apenas para estações que realmente necessitem de processamento gráfico adicional.

### 3.5 Dispositivos de entrada e saída

Recomenda-se utilizar periféricos adequados às atividades realizadas, incluindo:

* teclado;
* mouse;
* monitor com resolução adequada;
* headset quando necessário para comunicação;
* dispositivos de impressão conforme a necessidade operacional.

A utilização de monitores com boa resolução e periféricos adequados contribui para a ergonomia e produtividade dos usuários.

### 3.6 Componentes de rede

Recomenda-se uma infraestrutura de rede **Gigabit Ethernet**, utilizando switches gerenciáveis compatíveis com a segmentação por VLAN.

As estações de trabalho devem possuir interfaces de rede Gigabit Ethernet ou superiores quando necessário.

## 4. Configuração proposta

| Componente         | Configuração recomendada                   |
| ------------------ | ------------------------------------------ |
| Processador        | CPU intermediária atual, múltiplos núcleos |
| Memória RAM        | 16 GB                                      |
| Armazenamento      | SSD de 480/500 GB                          |
| Placa de vídeo     | GPU integrada                              |
| Rede               | Gigabit Ethernet                           |
| Monitor            | Resolução adequada ao ambiente corporativo |
| Sistema de entrada | Teclado e mouse                            |
| Áudio              | Headset quando necessário                  |

## 5. Justificativa técnica

A combinação de 16 GB de RAM e SSD proporciona uma melhoria significativa para computadores utilizados em atividades corporativas comuns.

O SSD reduz os tempos de acesso ao armazenamento, enquanto a memória RAM permite manter mais aplicações e processos ativos simultaneamente.

A utilização de processadores intermediários evita o custo adicional de componentes de alto desempenho que não seriam necessários para tarefas administrativas.

A adoção de GPU integrada também reduz o custo dos equipamentos, mantendo desempenho suficiente para as atividades previstas.

Na infraestrutura de rede, a utilização de Gigabit Ethernet e switches gerenciáveis permite maior capacidade de transmissão e possibilita a implementação de VLANs para segmentação lógica da rede.

## 6. Benefícios esperados

A configuração proposta pode proporcionar:

* redução do tempo de inicialização dos computadores;
* abertura mais rápida de aplicações;
* maior capacidade para execução simultânea de programas;
* melhoria da produtividade;
* maior estabilidade no uso dos sistemas corporativos;
* redução de gargalos relacionados ao armazenamento;
* melhoria da capacidade de comunicação da rede;
* possibilidade de segmentação da infraestrutura utilizando VLANs;
* melhor relação entre custo e desempenho.

## 7. Considerações

A configuração apresentada representa uma proposta de referência para computadores empresariais de uso geral.

A aquisição definitiva dos componentes deve considerar o levantamento dos equipamentos existentes, compatibilidade das peças, quantidade de usuários, aplicações utilizadas e orçamento disponível pela empresa.
