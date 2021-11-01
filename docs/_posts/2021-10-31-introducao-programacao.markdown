---
layout: post
title:  "Introdução à programação"
date:   2021-10-31 20:00:00 -0300
categories: "python"
author: Gabriel Carvalho Silva
---

Para que programar e como funciona?

## O que é computação?

De maneira geral, computação envolve o desenvolvimento de processos algorítmicos, ou seja, caminhos para alcançar algum objetivo, bem como sua teoria, análise, modelagem, eficiência, implementação e aplicação.

Abelson e Sussman, em *Structure and Interpretation of Computer Programs* dizem:

> Mathematics provides a framework for dealing precisely with notions of “what is.” Computation provides a framework for dealing precisely with notions of “how to".

Um **computador**, por sua vez, **é uma máquina que computa** informações conforme é programado. Um computador pode ser programado de muitas maneiras:

- Cartões perfurados
- Linguagens de Programação

## Programação e Linguagens de Programação

Vamos pensar na seguinte situação:

> *Precisamos resolver um problema do mundo real construindo uma solução computacional*

> Is this the real life or is this just fantasy? <br> Freddie Mercury

Um processo simplificado de análise e modelagem poderia ser:

1. Reconhecimento do problema
2. Análise do problema, entendendo quais os conceitos e que tarefas habitam no contexto estudado
3. Estruturação das informações a partir dos conceitos destacados e de relacionamentos entre elas
4. Descrição/Detalhamento das tarefas em processos, construindo dessa forma algoritmos.
5. Implementação

![imagem apresentando o processo de analise do problema](/assets/processo_analise_problema.jpg)

A etapa **1** se refere apenas ao momento em que estamos entendendo e abstraindo a situação estudada.

As etapas **2** e **3** por sua vez tem a função de explicitar as ideias que compõem o problema, a fim de que não sejam ignorados detalhes e informações importantes.

A etapa **4** é a definição dos processos para que o objetivo proposto seja alcançado. Um conjunto de processos pode ser entendido como um algoritmo e, no caso geral, podemos entender algoritmos como estruturas de natureza **procedural**, ou seja, em que as coisas acontecem passo a passo, conforme são definidas.

Podemos pensar em uma receita de *spaghetti*, por exemplo:

1. Esquentar a água
2. Quando ferver, salgar a água
3. Colocar o macarrão
3. Quando cozido, escorrer a água
5. Fim

Note, inclusive que `Quando ferver` e `Quando cozido` expressam condições de estado de um objeto (um dado) `água`, ou `macarrão`, enquanto `Esquentar`, `salgar`, `Colocar` e `escorrer` representam ações realizadas em cima desses objetos.

Isso poderia ser escalado. Uma receita de *spaghetti ao molho bechamel*, por exemplo, exigiria a definição de um outro algoritmo para descrever o preparo do molho bechamel.

A linguagem de programação ganha propósito na passagem da etapa **4** para a etapa **5**. É por meio dela que poderemos expressar ideias de maneira que o computador compreenda.

> *Mas como isso acontece? Como o computador entende o que eu escrevo? Um tio meu me contou que comptudaores só sabem zeros e uns...* <br> - *Aluno desesperado*

Bom, aqui temos um exemplo de código em Python:

```python
print("Quem e voce?")
nome = input()
print("Ola, " + nome + ", bem-vindx!")
```

Para uma entrada, digamos, `Josue`, a saída será:

```
Ola, Josue, bem-vindx!
```

De fato, lendo o código, como o computador sabe o que fazer?

Na verdade, a depender da linguagem, ou um compilador, ou um interpretador, será utilizado para converter aquilo que escrevemos em um "código de máquina", e é este o código que de fato será executado.

![imagem exemplificando o fluxo do interpretador](/assets/fluxo_interpretador.jpg)

