# Trabalho de Programação declarativa
## Aluno: Júlio César Alves

## Introdução
<p align="justify">Este trabalho tem como objetivo apresentar de forma simples e direta algumas sintaxes da linguagem declarativa Elixir. Também visando trazer alguns pontos de como se utilizar uma função na linguagem para os demais.
</p>

---

### O que é uma função?
<p align="justify">Uma função é a maneira que o programador tem de encapsular um código que poderá ser chamado por qualquer outro trecho de programa. Em resumo ele se parece muito com o que utilizamos na vida real com funções matematicas, com isso temos sempre uma definição com um nome e em seguida iremos chamar essa função definida anteriormente.</p>
<br>

### O que são os módulos em elixir?
<p align="justify">
Os módulos são responsáveis por manter e organizar as funções dentro de um namespace. Podendo definir, agrupar as funções tanto nomeadas quanto privadas de um código.</p>
<br>

#### Como se declara uma função Nomeadas em Elixir:
Uma função nomeada é dada pelo nome da váriavel, seus argumentos e o corpo da função. Ela pode ser utilizada de forma global entre os módulos, sendo acessada de qualquer parte do código.


<p align="justify">Para declarar uma função utilizamos o def em elixir, para entender melhor usaremos a seguinte sintaxe:</p>

``` 
  def nome_da_funcao(argumentos) do
   código a ser executado
  end
```


**do** nesse caso é usado para delimitar o corpo da função, o bloco de código que será executado quando a função for chamada.
<br>
<br>
#### Como se declarar funções anônimas em Elixir:
<p align="justify"> As funções anônimas são uma forma de criar e passar funções "inline" sem ter que dar-lhes um nome explícito. Elas podem ser usadas quando você precisa passar uma função como argumento para outra função ou atribuí-la a uma variável, mas não precisa de um nome para ela.

Sua declaração de sintaxe se da pelas palavras fn e end.Onde toda operação da função e atribuições serão feita entre ambas palavras na hora de declarar:</p>

```
nome_da_variavel = fn argumento1, argumento2 -> Código a ser executado 
end
```

#### Como se declarar funções privadas em Elixir:

<p align="justify">Está é responsável para quando não quisermos que as funções especificas não sejam acessadas globalmente em módulos, a gente a transforma em privada. Fazendo com que ela só pode ser acessada diretamente dentro de seu módulo e não mais globalmente. Ela sempre será declara antes da função pública, onde ela sempre será chamada dentro do módulo.

Ela é definida por defp, como será implementado no exemplo a baixo:</p>

```
defmodule MyModule do
  privada
  defp privada_func do
    # código da função privada
  end
```

----------

#### Códigos desenvolvidos:

*Um exemplo de Funções nomeadas*:
```
def soma(num1, num2) do
  num1 + num2
end

resultado = soma(2, 3)
```

<br>

*Um exemplo de Funções anônimas*:
```
soma = fn (num1, num2) -> num1 + num2 end
resultado = soma.(2, 3)

```

**Vamos observar algumas coisas**:

1. Podemos notar as variavéis num1 e num2 dentro de fn e end que determina a função anônima.
2. Soma aqui é o nome dado a váriavel anonima.
3. Para chamar a função basta passar os argumentos para a váriavel soma.
4. O ponto na linha de código soma.(2,3) está sendo usado para chamar a função anônima.
5. O código ele está somando dois números então quando atribui 2 e 3 o resultado final será 5. Assim como eu atribuir outros valores a num1 e num2.

<br>

*Um exemplo de Funções Privadas*:  
```
defmodule MyModule do
  privada
  defp privada_func(num1, num2) do
    num1 + num2
  end

  def public_func(num1, num2) do
    privada_func(num1, num2)
  end
end
```

**Vamos observar algumas coisas**:

1. Como citado a função defp ela está declarada dentro do modulo (defmodule MyModule).
2. Podemos notar que logo em seguida vem a função publica(global).
3. Nestre exemplo a função privada esta somando dois números. E só é possivel acessar ela dentro do módulo.
4. Public_func é a função pública que esta usando a privada.

---

#### Empresas e aplicativos que usam Elixir:

1. Adobe
2. Discord (Aplicativo)
3. Whatsapp (Aplicativo)
4. Pinterest

   <br>

#### Bibliotecas Recomendadas em Elixir:

__Plug__: 
<p align="justify">Recomendada para uso web, onde se utiliza para escrever servidores HTTP</p>


__Ecto__: 
<p align="justify">Utiliza-se para gerar códigos de migrações, definir modelos sobre tabelas de banco de dados e consultar e alterar os mesmo no banco.</p>


__Phoenix__: 
<p align="justify">O mesmo é um framework muito utilizado para a programação web em elixir. O mesmo tem suporte para rodar em plugs, assim gerando codigos de autenticação, cache, views, live code reloading, session management e outros.</p>

---

#### **Referências**:


* https://github.com/jaya/elixir-starter
* https://elixirschool.com/en/lessons/specifics/plug/
* https://elixirschool.com/en/lessons/specifics/ecto/
* https://coodesh.com/blog/candidates/carreiras/por-que-e-interessante-se-tornar-um-desenvolvedor-elixir/
