# Lista 1 - Revisão Probabilidade

<h2 align="center">Exercicio 1</h2>

#### Um dado equilibrado é lançado 2 vezes e os números obtidos nosdois lançamentos são registrados. 
#### Considere os seguintes eventos aleatórios:
- #### A = soma maior ou igual a 9.
- #### B = soma ímpar.
- #### C = um dos lançamentos foi 5.
- #### D = o mínimo entre as duas faces é 4.
#### Calcule as seguintes probabilidades:
#### P(A), P(B|C), P(A∩D) e P(C∪D).
<br/>

#### P(A)
```sh
  S = { {5,4} , {4,5} , {6,3} , {3,6}  , {5,5} , {6,4} , {4,6} ,  {6,5} , {5,6} ,  {6,6} }

  10 em 36 == 10/36 == 0.2777 == 27,77%
```

#### P(B|C)
```sh
# P(B)
  S  =  {{1,2}, {2,1}, {1,4}, {4,1}, {1,6}, {6,1}, {2,3}, {3,2}, {2,5},{5,2}, {3,4}, {4,3},{3,6},{6,3},{4,5},{5,4},{5,6},{6,5}}
  18 em 36 == 18/36 == 0.5 == 50%
# P(C)
  S = {{1,5},{2,5},{3,5},{4,5},{5,5},{6,5},{5,4},{5,3},{5,2},{5,1}}
  10 em 36 == 10/36 == 0.2777 == 27,77%
# P(B∩C) 
  6 em 36 == 6/36 == 0.1667 == 16.67%
  # P(B∩C) / P(B)
  0.1667 / 0.5 = 0.3333 == 33.33%

```	

#### P(A∩D)
```sh
  # P(A) 
    10 em 36 == 10/36 == 0.2777 == 27,77%
  # P(D) 
    S != {{1,1}, {1,2}, {2,1}, {2,2}}
    32 em 36 == 32/36 == 0.8889 == 88,89%
  # P(A∩D) 
    = P(A) = 27,77%
```

#### P(C∪D)
```sh
  # P(C)
    10 em 36 == 10/36 == 0.2777 == 27,77%
  # P(D) 
    S != {{1,1}, {1,2}, {2,1}, {2,2}}
    32 em 36 == 32/36 == 0.8889 == 88,89%
  # P(C∪D) 
    = P(D) = 88,89%
```

<hr/>

<h2 align="center">Exercicio 2</h2>

#### Um exame de sangue feito por um laboratório tem eficiência de 94% para detectar uma certa doença quando ela de fato existe. Entretanto, o teste aponta um resultado falso-positivo para 1% das pessoas sadias testadas (isto é, se uma pessoa testada for saudável, então, com probabilidade 0,01, o teste indicar á que a pessoa sadia tem a doença).  Se 0,4% da população tem a doença, qual é a probabilidade de uma pessoa ter a doença dado que o resultado de seu exame foi positivo?

```sh
P(A) pessoa doente = 0,04 
P(B) pessoa doente com resultado positivo = 0,94  
P(C) pessoa doente com resultado negativo = 0,06
P(D) pessoa saudavel com resultado positivo = 0,01 
P(E) pessoa saudavel com resultado negativo = 0,99
P(F) pessoa com resultado positivo = 0,04 * 0,94 + 0,996 * 0,01 = 0,004756

# pela formula P(doente | positivo) = P(doente ∩ positivo) / P(positivo)
(0,94 * 0,004) / 0,004756 = 0,7906 ~= 79%
```
<hr/>

<h2 align="center">Exercicio 3</h2>

#### Considere três urnas com as seguintes configurações: 
  - #### a urna I contém 6 bolas pretas, 3 brancas e 5 vermelhas;  
  - #### a urna II contém 4 bolas pretas, 4 brancas e 2 vermelhas; 
  - #### a urna III contém 4 bolas pretas, 2 brancase 7 vermelhas.  
#### Lança-se um dado equilibrado.  
  - #### Se sair 5, uma bola da urna I é retirada; 
  - #### se sair 1, 4, então uma bola da urna II é retirada;
  - #### se sair 2, 3 ou 6, então uma bola da urna III é retirada.
  <br/>

- #### (a)  Calcule a probabilidade da bola retirada ser vermelha.
- #### (b)  Calcule a probabilidade de ter sido sorteada a urna III, sabendo-se quea bola retirada foi vermelha.

```sh
  I.    6 Pretas; 3 Brancas; 5 Vermelhas
  II.   4 Pretas; 4 Brancas; 2 Vermelhas
  III.  4 Pretas; 2 Brancas; 7 Vermelhas

  P(I)   = 1/6 = 0,1667 = 16,67%
  P(II)  = 3/6 = 0,5    = 50%
  P(III) = 3/6 = 0,5    = 50%
  
  # (a)
  5/14 * 1/6 = 0,3572 * 0,1667 = 0,0595 = 5,9%
  2/10 * 3/6 = 0,2 * 0,5 = 0,066 = 6,6%
  7/13 * 3/6 = 0,5384 * 0,5 = 0,2692 = 26,92%
  P(V) = 39,42%

  # (b)
  P(III|V) = P(III ∩ V) / P(III) = 0,2692 / 0,5 = 0,5384 = 53,84%
```
<hr/>

<h2 align="center">Exercicio 4</h2>

#### Os amigos David Gilmour, Robert Plant, Nick Manson e Jimmy Page desejam fazer um amigo oculto entre eles. Calcule a probabilidade deque este amigo oculto não dê errado.
#### Obs:um amigo oculto dá errado quando uma pessoa sorteia ela mesma.

```sh
  4! * (1/2! - 1/3! + 1/4!) = 24 * (1/2 - 1/6 + 1/24)
  
  24 * ((3 - 1)/ 6 + 1/24)
  24 * (2/6 + 1/24)
  24 * ((8 + 1)/24) 
  24 * 9/24 = 9

  Logo a probabilidade de o amigo oculto não dê errado é 9/24 ou 37,5%
```
<hr/>

<h2 align="center">Exercicio 7</h2>

#### Consideremos o lançamento de dois dados equilibrados.  O espaço amostral desse experimento é formado pelos pares ordenados (i, j), em que i, j= 1,2,3,4,5,6.
#### Suponhamos que nosso interesse esteja no máximo das faces dos dois dados, isto é, vamos considerar a variável aleatória X que é dada por:
- #### X = o máximo das faces dos dois dados.
#### Assim,  por  exemplo,  se  o  resultado  do  experimento  foi  (2,4),  teremos que o valor de X neste ponto será 4, pois X (2,4) = máximo {2,4} = 4.
#### Análise similar nos permite afirmar que se o resultado do experimento foi (5,5), então X assumirá, neste ponto, o valor 5.  
#### Em relação a esta variável aleatória X, responda:
- #### (a)  Quais os valores que X assume?
- #### (b)  Para cada valor k que X assume, determine P(X=k).
- #### (c)  Calcule P(X <3) e P(X≥3).
- #### (d)  Calcule P(X >2|X <5).
- #### (e)  Esboce o gráfico da função de distribuição acumulada de X.

```sh
# a
{1,2,3,4,5,6}

# b
P(X = 1) = 1 / 36 = 0,028 = 2,8%
P(X = 2) = 2² - P(1) = 3/36 = 0,083 = 8,3%
P(X = 3) = 3² - P(1) - P(2) = 5/36 = 0,139 = 13,9%
P(X = 4) = 4² - P(1) - P(2) - P(3) = 7/36 = 0,194 = 19,4%
P(X = 5) = 5² - P(1) - P(2) - P(3) - P(4) = 9/36 = 0,25 = 25%
P(X = 6) = 6² - P(1) - P(2) - P(3) - P(4) - P(5) = 11/36 = 0.306 = 30,6%

# c
P(X < 3) = 1/36 + 3/36 = 4/36 = 0,1111 = 11,11%
P(X >= 3) = 32/36 = 0,8889 = 88,89%

# d 
P(X > 2 | X < 5) = P(X > 2 ∩ X < 5) / P(X > 2)
= (12/36) / (32/36) = 0.3333 / 0,8889 = 0,3749
= 37,49%

```