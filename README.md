---
marp: true
theme: default
_class: lead
paginate: true
backgroundColor: #fff
---

# Análise de Algoritmos e Entrevistas Técnicas

### Professores: 
Fabio Lubacheski ([fabioagl@insper.edu.br](mailto:fabioagl@insper.edu.br))
Leonardo Moraes ([leonardomm8@insper.edu.br](mailto:leonardomm8@insper.edu.br))

---

# Critério de avaliação

Para ser aprovado, o aluno deve obter **Média Final (MF)** maior ou igual a **5**. 

$MF = 0,7*Provas + 0,2 * APS + 0,1 * Entrevistas$

A **Média das Provas (MP)** é calculada conforme abaixo

$MP =  MAX((P1 + 2*P2 + 4*P3)/7, ((3*P2 + 4*P3)/7)$

Em caso de **avaliação substitutiva**, a nota substituirá a prova que maximizar a média final.

---

# Delta

Ao final do semestre, caso o aluno possua **média final maior ou igual a 5**, mas estiver bloqueado por um critério de barreira de aprovação (**média das provas menor que 5**), a **prova substitutiva** será considerada como **prova delta**. A **nota da delta deve ser maior ou igual a 5** para a aprovação na disciplina. Caso contrário, o aluno estará reprovado na disciplina (mesmo que tiver média superior a 5).

--- 

# Bibliografia básica
![bg right:50%](img/livro.jpg)
### Algoritmos: Teoria e Prática
### CORMEN, T. H.; LEISERSON, C. E.; RIVEST, R. L; STEIN, C.
### site: http://mitpress.mit.edu/algorithms/

## Este livro é realmente muito importante para disciplina!

---

# O que iremos aprender na disciplina ?

* Nessa disciplina iremos aprender a medir a eficiência de algoritmos, ou seja, calcular o **tempo de execução** do algoritmo.

* A partir do **tempo de execução** do algoritmo é possível comparar algoritmos que resolvam um mesmo problema.


---
# Como calcular o **tempo de execução** do algoritmo ? 

> Para obter o **tempo de execução** de um algoritmo poderíamos implementar o algoritmo e realizar vários testes para várias entradas. Mas ai surge algumas questões:

* O hardware (memória,  processador, disco, etc..) influencia ? 

* E qual a influência do software (SO, linguagem de programação, compilador, código é intretado, etc ) ?

* Nesse caso, você estaria comparando **implementações**, e não **algoritmos**.


---
# Como calcular tempo de execução (complexidade de tempo) ?

* Em vez de perguntar

    * "**Quantos segundos** o algoritmo demora?"

* Perguntamos
 
    * "**Quantas operações** o algoritmo executa em função do tamanho da entrada?"


---
# Algorimo que soma elementos de um vetor

Essa mudança de perspectiva elimina detalhes que não são essenciais para a análise. Por exemplo:

```text
Soma-Vetor(A)
1. soma = 0
2. n = |A|
3. para i = 1 até n
4.     soma = soma + A[i]
5.     i = i + 1
6. retorne soma
```
* Nesse caso não estamos considerando **se**:
    * a soma demora $1 ns$ ou $5 ns$;
    * o código foi escrito em `C`, `Java` ou `Python;
    * o processador possui *cache L3*.

---
# Formalizando a contagem de operações do algoritmo

O que importa é que o laço é executado aproximadamente **n** vezes.

Assim, modelamos o **tempo de execução** por uma função do **tamanho da entrada**, como:

$T(n) = an + b$

onde:
    $a$ representa o custo constante de cada iteração;
    $b$ representa o custo fixo antes e depois do laço.

---

# Contagem de operações do algoritmo
Agora vamos contar aproximadamente as operações.

| Operação             | Quantidade |
| -------------------- | ---------: |
| `soma = 0`           |          1 |
| `i = 1`              |          1 |
| teste `ate  n`       |      n + 1 |
| incremento de `i`    |          n |
| `soma = soma + A[i]` |          n |
| `i = i + 1`          |          n |
| `retorna soma`       |          1 |


---
# Abstração em Análise de Algoritmos
Somando tudo:
$T(n)=1+1+(n+1)+n+n+n+1$

ou

$T(n)=4n+4$
$a=4$ 
$b=4$

* concluímos que sua complexidade assintótica é $O(n)$.

---

# Abstração em Análise de Algoritmos

Na Análise de Algoritmos, a abstração consiste em ignorar os detalhes específicos da implementação — como linguagem de programação, compilador e hardware — e representar o **custo de um algoritmo apenas em função do tamanho da entrada**. Essa abstração permite comparar algoritmos de maneira geral, utilizando funções matemáticas e notações assintóticas, como $O$, $Θ$ e $Ω$.

---

# **Obrigado !**