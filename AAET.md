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

* A partir do **tempo de execução do algoritmo** é possível comparar algoritmos que resolvam um mesmo problema.

* Como calcular o **tempo de execução** do algoritmo ?




---
# Tempo de execução (complexidade de tempo)

> Para obter o **tempo de execução** de um algoritmo poderíamos implementar o algoritmo e realizar vários testes para várias entradas. Mas ai surge algumas questões:

* O hardware (memória,  processador, disco, etc..) influencia ? 

* E qual a influência do software (SO, linguagem de programação, compilador, código é intretado, etc ) ?

* Nesse caso, você estaria comparando **implementações**, e não **algoritmos**.


---
# Abstração em Análise de Algoritmos

* Em vez de perguntar

    * "Quantos **segundos** o algoritmo demora?"

* Perguntamos
 
    * "Quantas **operações** o algoritmo executa em função do tamanho da entrada?"


---
# Abstração em Análise de Algoritmos

Essa mudança de perspectiva elimina detalhes que não são essenciais para a análise. Por exemplo:
```text
Soma-Vetor(A)
1. soma = 0
2. para j = 1 até |A|
3.     soma = A[j]
4. retorne soma
```
* Não importa se:
    * a soma demora 1 ns ou 5 ns;
    * o código foi escrito em C, Java ou Python;
    * o processador possui cache L3.
* O que importa é que o laço é executado aproximadamente **n** vezes.

---
# Abstração em Análise de Algoritmos

* Assim, modelamos o **tempo de execução** por uma função do **tamanho da entrada**, como:

    * $T(n) = an + b$

    * concluímos que sua complexidade assintótica é $O(n)$.
---

# Abstração em Análise de Algoritmos

Na Análise de Algoritmos, a abstração consiste em ignorar os detalhes específicos da implementação — como linguagem de programação, compilador e hardware — e representar o **custo de um algoritmo apenas em função do tamanho da entrada**. Essa abstração permite comparar algoritmos de maneira geral, utilizando funções matemáticas e notações assintóticas, como O, Θ e Ω.

---

# **Obrigado !**