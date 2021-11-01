---
layout: post
title:  "Primeiros passos com Python - Variáveis, entrada e saída de dados"
date:   2021-10-31 20:00:00 -0300
categories: "python"
author: Gabriel Carvalho Silva
---

## A linguagem Python
---
Uma breve apresentação e contextualização de uma das linguagens mais populares no mundo

- Lançada por Guido van Rossum em 1991.
- Projetada com a filosofia de enfatizar a importância do esforço do programador sobre o esforço computacional priorizando a legibilidade do código sobre a velocidade ou expressividade.
- É versátil e relativamente fácil de se aprender. Possui sintaxe muito próxima do inglês falado.


## Principais características da linguagem

- Interpretada (pode ser utilizada em qualquer ambiente que possua um interpretador python instalado
- Tipagem de variáveis fraca e dinâmica


## Elementos básicos da linguagem
---

### Comentários no codigo

Comentários são úteis para descrever o funcionamento do código, ou simplesmente anotar coisas no arquivo de código e essencialmente podem ser feitos no código de duas maneiras:

```python
# isso é um comentário de uma linha

"""
Já este aqui pode 
ter
várias
linhas
muitas linhas
"""

```

> comentários são ignorados pelo interpretador

### Variáveis

Variáveis podem ser abstraídas como caixinhas onde armazenamos informações. Podem ser utilizadas em expressões matemáticas, funções, etc.

Por convenção da comunidade Python, nomes de variáveis seguem o padrão:

```python
variavel = 10 # sempre minusculo
outra_variavel = 20 # underscore separa nomes compostos
```

> Nomes de variáveis que sejam palavras reservadas da linguagem (conferir documentação) não serão permitidas pelo interpretador.

### Tipos

A tipagem é fraca e dinâmica, o que significa que variáveis são associadas aos tipos em tempo de execução e podem mudar de tipo a depender do valor que recebem.

### Constantes e os tais _"Literais"_

Valores "brutos" são entendidos como constantes da linguagem, ou valores literais, pois são... _literalmente_ um valor, e não uma variável onde guardamos um valor. 

Variáveis guardam valores, e as utilizamos como se fossem os valores, pois o interpretador as substitui pelos valores que guardam, porém não são valores em si e sim objetos por si só.

Por exemplo, podemos altera o valor armazenado em uma variável, mas o objeto nunca foi alterado:

Diagmos que temos uma variável que guarda do saldo de um cliente no banco. Chamaremos essa variável de `saldo` e ela deve armazenar valores reais. Inicialmente ela guarda o valor 300.0, após a realização de um saque, o valor é alterado para 250.0. O valor armazenado foi alterado, mas a "caixa" ainda é a mesma.

Obs.: Aqui `objeto` não está realacionado com a ideia de programação orientada a objeto. Nesse contexto, `objeto` se refere apenas à uma entidade computacional, ou ideia que manipulamos.

//imagem do trem la

```python
print("ola") #podemos utilizar texto literal diretamente
```

### Strings e concatenação de Strings

Texto é um tipo de dado muito utilizado e por isso é importante saber como podemos trabalhar com ele.

Existem caracteres especiais que expressam símbolos diferentes do que estamos acostumados na linguagem escrita. Por exemplo: '\n' representa uma nova linha e '\t' uma tabulação (espaços definidos pela tecla `tab`)

```python
print("Esse texto tem\n\tduas linhas mas a segunda é tabulada")
```

As vezes é interessante unir strings de alguma forma. Podemos fazer isso essencialmente de duas formas: por concatenação, ou por interpolação.

*Concatenar* significa simplesmente unir texto

Podemos utilizar o operador '+' ou, no caso da função print(), podemos utilizar o separador (vírgula).

```python
nome = "Josue"
sobrenome = "O cachorro do mal"

# A virgula, por padrao, separa os parametros com um espaço vazio (" ")
print(nome, sobrenome)

# Aqui fazemos essencialmente a mesma coisa, porém manualmente
nome_completo = nome + " " + sobrenome
print(nome_completo)

# Tambem poderiamos diretamente fazer:
print(nome + " " + sobrenome)

```

```python
dia = 12
mes = 11
ano = 2021

# Podemos utilizar format() para "injetar", ou melhor, interpolar, valores na string original
# os valores susbstituem em ordem os respectives pares de chaves ("{}")
data_formatada = "Data de hoje: {}/{}/{}".format(dia, mes, ano)

print(data_formatada)

```

### Operadores e precedência

*Atribuição*

o operador `=` é chamado de operador de **atribuição**.
A expressão à direita, após resolvida, é associada ao objeto à esquerda, que armazena o valor resolvido.

```python
import math as calculator

# coeficientes de f(x) = 3x^2 + 2x - 10
a = 3
b = 2
c = -10

d = (b * b) - (4 * a * c) # primeiro é resolvida a expressao a direita, e depois atribuido o resultado à variavel d
r1 = (-b + calculator.sqrt(d)) / (2 * a)
r2 = (-b - calculator.sqrt(d)) / (2 * a)

print("As raizes da funcao sao:\n\t Raiz 1 = {}\n\t Raiz 2 = {}".format(r1, r2)) 

```

*Aritmética*

Adição (+)

```python
10 + 2 # resulta em 12
```

Subtração (-)


```python
10 - 2 # resulta em 8
```

Multiplicação (*)


```python
10 * 2 # resulta em 20
```

Divisão (/)


```python
10 / 2 # resulta em 5
```

Divisão modular (%)


```python
10 % 8 # resulta em 2
```

"Floor division" (//)

```python
13.0 / 2 # resulta em 6.5
13.0 // 2 # resulta em 6
```

Exponenciação (**)

```python
10 ** 2 # resulta em 100
```

*Lógica e comparação*

Podemos guardar valores lógicos (booleans) em variáveis. Mas, além disso, podemos também utilizar operadores para combinar e estabelecer expressões lógicas mais complexas.

**and**

```python
>>> True and True
True
>>> True and False
False
>>> False and False
False
>>> False and True
False
```

or

```python
>>> True or True
True
>>> True or False
True
>>> False or False
False
>>> False or True
True
```

not

```python
>>> not True
False
>>> not False
True
```

Além desses operadores, temos também operadores de **comparação** que resultam em algum valor lógico (`>`, `<`, `==`, `!=`, `>=` e `<=`).

Obs.: `==` é diferente de `=`. O operador `==` testa para igualdade, enquanto `=` é o operador de atribuição de valor (**em outras linguagens**, para evitar a confusão, o operador de atribuição é `:=`)

Extra: `is` e `is not` servem para testar igualdade entre "referências", mas isso não é importante agora...

```python
data_aniversario = "19/10"
data_atual = "15/11"

if(data_aniversario == data_atual):
    print("Feliz aniversario")
else:
    print("Apenas mais um dia normal")

```

```python
data_aniversario = "19/10"
data_atual = "19/10"

if(data_aniversario == data_atual):
    print("Feliz aniversario")
else:
    print("Apenas mais um dia normal")
```

Extra: Podemos combinar operadores aritméticos com o operador de atribuição

```python
num = 1
num = num + 1

print(num)
```

```python
num = 1
num += 1

print(num)
```

### Entrada e Saída de dados

*Escrever informações na tela*

A função print() escreve na saída padrão (normalmente a tela), o conteúdo que lhe é passado.

Essa função possui dois argumentos especiais, o `sep` e o `end`.

```python
# Podemos "printar" texto como ja fizemos antes
print("Ola PEG!")

#tambem podemos escrever o valor de uma variavel
x = 10
print(x)

#ou de uma expressao...
print(10 + 2)

# ou misturar as coisas

print("O valor de x eh:", x) # aqui a virgula coloca um espaço vazio

# mas podemos mudar isso...
dia = 19
mes = 10
ano = 2000

print("Data de nascimento:", end = " ") # aqui alteramos tambem o final do que eh escrito, retirando a nova linha automatica
print(dia, mes, ano, sep = "/") # alterando o valor de 'sep' alteramos o comportamento da virgula na chamada de print()
```

*Receber informações e interação com o usuário*

A função `input()` retorna o valor informado pelo usuário e pode ser atribuído à uma variável, por exemplo

```python
input()
```

```python
# mas para utilizar esse valor precisamos guardar em algum lugar...

x = input() # x guarda o valor isnerido pelo usuario

print("Voce inseriu", x)
```
