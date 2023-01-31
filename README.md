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

<p align="justify">Para declarar uma função utilizamos o def em elixir, para entender melhor usaremos a seguinte sintaxe:</p>

``` 
  def nome_da_funcao(argumentos) do
   código a ser executado
  end
```


**do** nesse caso é usado para delimitar o corpo da função, o bloco de código que será executado quando a função for chamda.
<br>
<br>
#### Como se declarar funções anônimas em Elixir:
<p align="justify">Funções anonimas como seu nome diz elas geralmente não tem nomes especificos. Elas são utilizadas para passar funções para outras funções de maneira mais rápida, sem precisar declarar inúmeras vezes por exemplo uma caracteristica para uma função, você geraria uma nova que faria esse papel de dar as caracteristicas. As mesmas são dadas como de primeira classe, em outras palavras isso é, podem ser passadas como argumentos para outras funções e também servir de retorno.

Sua declaração de sintaxe se da pelas palavras fn e end.Onde toda operação da função e atribuições serão feita entre ambas palavras na hora de declarar:</p>

```
nome_da_variavel = fn argumento1, argumento2 -> Código a ser executado 
end
```

<p align="justify">Lembrando que se eu considerar parametro1 = a, parametro2 = b, e desejar fazer a soma deles, iria acrescentar ao corpo da função nome_da_váriavel.(4, 5), o resultado seria: 9, pois estou considerando a = 4 e B = 5. Também podemos afirmar que dentro de um map consigo acessar todos os dados apenas em uma linha ou duas de código acrescentando uma função anonima.</p>
<br>

#### Como se declarar funções privadas em Elixir:

<p align="justify">Está é responsável para quando não quisermos que as funções especificas não sejam acessadas globalmente em módulos, a gente a transforma em privada. Fazendo com que ela só pode ser acessada diretamente dentro de seu módulo e não mais globalmente.

Ela é definida por defp, como será implementado no exemplo a baixo:</p>

```
Codigo exemplo
```

----------

#### Código desenvolvido:

Replit: 


---

#### Bibliotecas Recomendadas em Elixir:

__Plug__: 
<p align="justify">Recomendada para uso web, onde se utiliza para escrever servidores HTTP</p>


__Ecto__: 
<p align="justify">Utiliza-se para gerar códigos de migrações, definir modelos sobre tabelas de banco de dados e consultar e alterar os mesmo no banco.</p>


__Phoenix__: 
<p align="justify">O mesmo é um framework muito utilizado para a programação web em elixir. O mesmo tem suporte para rodar em plugs, assim gerando codigos de autenticação, cache, views, live code reloading, session management e outros.</p>

---

#### **Créditos**:


* https://github.com/jaya/elixir-starter
* https://elixirschool.com/en/lessons/specifics/plug/
* https://elixirschool.com/en/lessons/specifics/ecto/
