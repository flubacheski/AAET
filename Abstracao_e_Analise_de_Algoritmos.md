# Abstração e sua relação com a Análise de Algoritmos

## O problema

Ao comparar algoritmos, não basta medir o tempo de execução em segundos,
pois esse tempo depende de diversos fatores, como:

-   Processador (Intel, AMD, ARM etc.);
-   Quantidade de memória RAM;
-   Memória cache;
-   Sistema operacional;
-   Compilador;
-   Linguagem de programação;
-   Otimizações aplicadas.

Nesse caso, estaríamos comparando **implementações**, e não
**algoritmos**.

## A abstração

Na Análise de Algoritmos fazemos uma abstração desses fatores.

Em vez de perguntar:

> "Quantos segundos o algoritmo demora para executar?"

Perguntamos:

> **Quantas operações o algoritmo executa em função do tamanho da
> entrada?**

Essa mudança de perspectiva elimina detalhes que não são essenciais para
a análise.

Por exemplo:

``` c
for (i = 0; i < n; i++)
    soma += v[i];
```

Não importa se:

-   a soma demora 1 ns ou 5 ns;
-   o código foi escrito em C, Java ou Python;
-   o processador possui cache L3.

O que importa é que o laço é executado aproximadamente **n** vezes.

Assim, modelamos o tempo de execução por uma função do tamanho da
entrada, como:

**T(n) = an + b**

e concluímos que sua complexidade assintótica é **Θ(n)**.

## O que abstraímos?

Na disciplina, normalmente abstraímos:

-   Hardware;
-   Linguagem de programação;
-   Compilador;
-   Constantes multiplicativas;
-   Pequenos custos fixos.

O foco passa a ser apenas o crescimento do custo computacional.

## O que permanece na análise?

Mantemos apenas os aspectos que realmente influenciam a eficiência
assintótica:

-   Número de comparações;
-   Número de atribuições;
-   Número de chamadas recursivas;
-   Número de iterações;
-   Quantidade de memória utilizada.

## Exemplo

**Algoritmo A**

``` c
for (i = 0; i < n; i++)
    soma += v[i];
```

**Algoritmo B**

``` c
for (i = 0; i < n; i++)
    for (j = 0; j < n; j++)
        soma += v[i];
```

Independentemente do computador utilizado:

-   O Algoritmo A executa aproximadamente **n** operações.
-   O Algoritmo B executa aproximadamente **n²** operações.

A abstração permite concluir que o Algoritmo A é assintoticamente mais
eficiente que o Algoritmo B sem precisar executá-los.

## Definição

> **Na Análise de Algoritmos, a abstração consiste em ignorar os
> detalhes específicos da implementação --- como linguagem de
> programação, compilador e hardware --- e representar o custo de um
> algoritmo apenas em função do tamanho da entrada. Essa abstração
> permite comparar algoritmos de maneira geral, utilizando funções
> matemáticas e notações assintóticas, como O, Θ e Ω.**

## Analogia

Uma analogia útil é comparar automóveis pelo **consumo de combustível
(km/L)**, e não pelo tempo necessário para percorrer um trajeto
específico.

O tempo depende de fatores externos, como trânsito, estrada e motorista.
Já o consumo é uma característica mais geral do veículo.

Da mesma forma, a Análise de Algoritmos compara o **crescimento do custo
computacional**, e não o tempo medido em uma máquina específica.
