# 
Análise de Algoritmos e Entrevistas Técnicas
## Objetivos

1. Identificar e demonstrar a complexidade de espaço e tempo de um algoritmos utilizando notação assintótica;
2. Projetar e implementar algoritmos determinísticos, probabilísticos, dinâmicos e gulosos;
3. Descrever as intuições e funcionamento de algoritmos no contexto de entrevistas técnicas de programação.

## Conteúdo Programático

- **Notação assintótica:** crescimento de funções, ordens de complexidade de algoritmos, pior caso, melhor caso e caso médio
- **Demonstrações de propriedades de notação assintótica**
- **Análise de algoritmos determinísticos:** algoritmos iterativos e recursivos, análise de algoritmos iterativos e recursivos clássicos para ordenação e busca
- **Análise de programação dinâmica:** programação dinâmica, algoritmos dinâmicos clássicos, análise de algoritmos dinâmicos
- **Análise de algoritmos gulosos**
- **Análise de algoritmos probabilísticos:** algoritmos probabilísticos, distribuições para entradas, análise probabilística de algoritmos determinísticos, análise probabilística de algoritmos probabilísticos
- **Entrevistas técnicas:** estrutura, entrevistas nacionais e internacionais, prática em entrevistas técnicas

## Aprovação

Para ser aprovado, um aluno deve obter $NF \geq 5$.

$$NP = 0.7 \cdot MP + 0.3 \cdot APS$$

$$NF = \min(10, NP + \text{Bônus} \cdot I\{\text{Proficiente}\})$$

- $NP$ - nota parcial;
- $NF$ - nota final;
- $MP$ - média de provas:
  - Precisa ser maior ou igual a 5;
  - $MP = \frac{PI + 3\cdot PF}{4}$
- $APS$ - atividades de sala e problemas para casa:
  - Serão feitas no PrairieLearn;
  - É possível entregar atrasado, mas haverá desconto na nota. As datas estão especificadas no PrairieLearn.
  - $APS = \frac{\sum\limits_{i}^n \text{Módulo}_i - \min(\text{Módulo}_1, \dots ,\text{Módulo}_n)}{n-1}$ (em outras palavras, é a média dos módulos descartando a menor nota).
  - Para o cálculo das notas dos módulos será utilizada o seguinte mapeamento (sobre o qual poderá ser aplicado o desconto por atraso):
    | Insuficiente | Em Desenvolvimento | Essencial | Proficiente | Avançado |
    | :----------: | :----------------: | :-------: | :---------: | :------: |
    | 0 | 2 | 5 | 8 | 10 |
- $\text{Bônus}$ - vídeo sobre algum dos conteúdos extras:
  - Vale até $1.0$ ponto extra;
  - Só vale se já possuir $NP$ maior ou igual a 7.
- $I\{\text{Proficiente}\} = \left\{\begin{array}{ll}1 & \text{se } NP \geq 7 \\ 0 & \text{c.c.}\end{array}\right.$

## Módulos

### 1. Definições e demonstrações básicas (4 aulas)

#### Nível Essencial

- Definição de $O$, $\Omega$, $\Theta$ e primeiras demonstrações
  - Explain in plain English
  - Demonstrações de algumas propriedades básicas
  - Demonstrações de complexidades simples
- Análise do Insertion Sort

#### Nível Proficiente

- Análise do Bubble Sort ($\Omega$ e $O$) e Selection Sort ($\Theta$)

#### Nível Avançado

- Counting sort, radix sort, bucket sort
- Implementação do insertion sort

### 2. Entrevista 1 (3 aulas)

Entrevistas sobre listas ligadas: preparação, entrevistas e discussão
Depois mudar para tabelas de hash

### PROVA 1

### 3. Divisão e Conquista (4 aulas)

#### Nível Essencial

- Análise da busca binária
  - Olhar código fonte do `binarySearch` do Java
  - Análise de algoritmo da busca binária em Java
- Merge sort

#### Nível Proficiente

- Multiplicação de matrizes

#### Nível Avançado

- Resolvendo recorrências
  - Teorema mestre?
- **OU** Implementar mergesort em C, Java e Python e comparar os tempos para entradas de vários tamanhos

### 4. Entrevista 2 (2 aulas)

Entrevistas sobre tabelas de hash
Depois mudar para: Entrevistas sobre divisão e consquista (recursão).

### PROVA 2

### 5. Programação Dinâmica (4 aulas)

#### Nível Essencial

- Fibonacci (demonstração da complexidade exponencial): exponencial para linear
- Elementos da programação dinâmica

#### Nível Proficiente

- Edit distance (Levenshtein): https://jeffe.cs.illinois.edu/teaching/algorithms/book/03-dynprog.pdf
- Rod cutting

#### Nível Avançado

- Longest Common Subsequence

### 6. Entrevista 3 (2 aulas)

Entrevistas sobre programação dinâmica

### 7. Análise probabilística e algoritmos com aleatorização (4 aulas)

Pré-módulo: vídeo sobre Hire-Assistant algorithm

#### Nível Essencial

- Randomly-permute
- Simulação do Hire-Assistant: implementar código usando randomly-permute e executar várias vezes

#### Nível Proficiente

- The birthday paradox
- The online hiring problem

#### Nível Avançado

- Análise do quicksort determinístico
- Quicksort com pivot aleatório

### 8. Entrevista 4 (2 aulas)

Entrevistas sobre algoritmos gulosos

### PROVA 3

### 9. Algoritmos Gulosos (4 aulas)

#### Nível Essencial

- Activity selection problem: https://jeffe.cs.illinois.edu/teaching/algorithms/book/04-greedy.pdf
- Elementos da estratégia gulosa

#### Nível Proficiente

- Greedy vs. dynamic programming

#### Nível Avançado

- Huffman codes

### 10. Medianas e estatísticas de ordem (2 aulas)

#### Nível Essencial

- Simultaneous minimum and maximum

#### Nível Proficiente

- Selection in expected linear time

#### Nível Avançado

- Selection in worst-case linear time

### 11. EXTRA Comunicação (1 aula)

Exercícios de descrição de algoritmos em uma frase

## Extras

- Listas ligadas
- Atividade sobre recursão
- String matching (KMP)
- Lower bounds for sorting (8.1)
- Union find
- Discussão knapsack 0-1 vs. fractional
- Análise amortizada:
  - Análise agregada: multipop stack
  - Accounting method: table expansion
