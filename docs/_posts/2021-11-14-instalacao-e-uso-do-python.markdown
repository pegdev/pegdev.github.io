---
layout: post
title:  "Instalação e uso do Python"
date:   2021-11-14 23:00:00 -0300
categories: "python"
author: Felipe Raimundo dos Santos e Gabriel Carvalho Silva
---

## O que precisamos?

Python é uma linguagem interpretada, o que significa que precisamos de um interpretador Python instalado para executar *scripts*, ou executar comandos pelo *ambiente interativo*.

## Instalação do Python

### Windows

### Linux

Muitas distribuições Linux já vem acompanhadas do interpretador Python. Para verificar se é o seu caso, execute:

```shell

python --version

```

ou

```

python3 --version

```

Caso não esteja instalado, prossiga com as intruções a seguir:

#### Terminal

##### Distribuição Debian e derivados (Ubuntu, Mint, Pop, etc.)

Abra o terminal e execute o seguinte comando:

```shell

sudo apt install python3

```

Além disso, para instalar o IDLE (ambiente de desenvolvimento integrado padrão do Python), execute:

```shell

sudo apt install idle3

```

Você pode é claro, utilizar outras IDEs, como o PyCharm da Jetbrain, o Anaconda, Spyder, ou ainda utilizar editores de texto como um bloco de notas, o **vim**, **visual studio code**, **sublime**, ou outros.

##### Distribuição Arch e dervados (Manjaro, ArcoLinux, etc.)

Abra o terminal e execute:

```shell

sudo pacman -S python

```

O IDLE já está incluido, porém necessita do tkinter para funcionar, para isso instale-o separadamente ou ao mesmo tempo que o Python.

```shell

sudo pacman -S tk

```

ou

```shell

sudo pacman -S python tk

```

#### Tarball

Menor prático, porém ainda possivel. 
Visite o *site* https://www.python.org/ e no menu **Downloads** escolha a versão que deseja instalar.

[Imagem com o trem circulado]

Após fazer o *download* do arquivo tar, descomprima-o e siga as intruções no arquivo README.


## Utilização do Python

Podemos utilizar o Python essencialmente de três maneiras: executando scripts python, utilizando a interface interativa, ou por *notebooks* (como Jupyter ou Google Colab).

### Scripts

Executar scripts python consiste basicamente em passar ao interpretador um arquivo .py como argumento.

```shell

~ >>> cat script.py                                                            
def boo():
    print("boo")

def foo():
    print("foo")

#boo e foo identificam os objetos de funcao

function_collection = {"boo": boo, "foo": foo}

function_collection["boo"]()


~ >>> python script.py                                                         
boo
~ >>> 

```

O comando `cat` nos mostra o que há no arquivo. Executamos então o python por meio do comando `python` (pode ser `python3` em ambientes Debian) passando como argumento **script.py**, nosso script python (como o nome sugere). Esse arquivo pode ter qualquer nome, é necessário apenas que a sintaxe da linguagem esteja correta no conteúdo do arquivo, pois do contrário resultará em erro.

### Python Shell

A interface interativa, também chamada **Python Shell**, permite executar código Python tendo como respostas, "retornos", as resoluções do interpretador. Para abrir a interface, basta executar `python -i`, ou o comando `python` sem passar qualquer argumento.

```shell

~ >>> python -i                                                                
Python 3.9.7 (default, Aug 31 2021, 13:28:12) 
[GCC 11.1.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 10
10
>>> x = 10
>>> x
10
>>> print(x)
10
>>> print()

>>> print
<built-in function print>
>>> 

```

**Obs.:** O IDLE inclui um editor de *scripts* (bem como um botão para executar o *script*), e também uma janela com o *python shell* (que é a janela inicial padrão).
