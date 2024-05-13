# Atividade Avaliativa de Cálculos de Área

Este repositório é dedicado à atividade avaliativa de cálculos de área, correspondente à quarta semana da segunda sprint do segundo módulo do [Inteli - Instituto de Tecnologia e Liderança](https://www.inteli.edu.br/). O foco desta atividade é a **matemática e a física**. Neste contexto, aceitamos o desafio de explorar como as integrais indefinidas e definidas podem ser aplicadas em problemas de aplicação web.

## Problema 1 – Modelagem do Crescimento de Usuários em uma Aplicação Web

Suponha que você seja um analista de dados de uma aplicação web e está encarregado de modelar o crescimento de usuários ao longo do tempo. Você coletou dados que sugerem que o número de usuários ativos na aplicação web aumenta de acordo com a função $f(t) = 50e^{0.1t}$, onde  $t$ é o tempo em meses desde o lançamento da aplicação e $f(t)$ é a taxa de crescimento (em milhares de pessoas por mês).

Vamos definir $F(t)$ como a função que representa a integral indefinida de $f(t)$ em relação a $t$. Note que $F(t)$ é o número total de usuários (em milhares) que se juntaram à aplicação web desde seu lançamento, ou seja, nos fornece a função acumulada de usuários ao longo do tempo.

### a) Com auxílio de software, faça o gráfico da função f(t) para t<30.

Nós geramos o gráfico da função $f(t) = 50e^{0.1t}$ para $t < 30$ utilizando a biblioteca [Matplotlib](https://matplotlib.org/) na plataforma Python. O código a seguir foi usado para criar o gráfico:

```python
import matplotlib.pyplot as plt
import numpy as np

t = np.linspace(0, 30, 100)
f_t = 50 * np.exp(0.1 * t)

plt.plot(t, f_t)
plt.title('Gráfico de $$f(t) = 50e^{0.1t}$$')
plt.xlabel('Tempo (meses)')
plt.ylabel('Taxa de crescimento (milhares de pessoas por mês)')
plt.grid(True)
plt.show()
```

Este código cria um conjunto de valores para t variando de 0 a 30, calcula os correspondentes valores de $f(t)$, e então plota $f(t)$ versus $t$. O resultado é um gráfico que visualiza como a taxa de crescimento de usuários muda ao longo do tempo.

![Gráfico de f(t)](assets/grafico.png)

### b) Determine o número de meses necessário para dobrar a taxa de crescimento inicial do número de usuários da aplicação web.

Para determinar o número de meses necessário para dobrar a taxa de crescimento inicial do número de usuários da aplicação web, precisamos resolver a equação $50e^{0.1t} = 2 * 50$ para $t$. Isso nos dá:

$$
50e^{0.1t} = 100
$$

Dividindo ambos os lados por 50, obtemos:

$$
e^{0.1t} = 2
$$

Aplicando o logaritmo natural de ambos os lados, obtemos:

$$
0.1t = \ln(2)
$$

Finalmente, resolvendo para $t$, obtemos:

$$
t = \frac{\ln(2)}{0.1} \approx 6.93 \, \text{meses}
$$

### c) Encontre a função F(t). Discuta o significado da constante que aparecerá na integração indefinida. O que é necessário saber para definir o valor da constante?

A função $F(t)$ é a integral indefinida de $f(t)$. Portanto, temos:

$$
F(t) = \int f(t) dt
$$

Substituindo $$f(t)$$, obtemos:

$$
F(t) = \int 50e^{0.1t} dt
$$

A integral de $50e^{0.1t}$ é $500e^{0.1t}$, então temos:

$$
F(t) = 500e^{0.1t} + C
$$

onde $C$ é a constante de integração. O valor de $C$ depende das condições iniciais do problema. No nosso caso, como o número de usuários era nulo no lançamento da aplicação, temos:
$C = 0$

A constante de integração representa o valor inicial da função acumulada de usuários ao longo do tempo. Se tivéssemos um número diferente de usuários no lançamento da aplicação, esse número seria representado pela constante $C$.

### d) Quantos meses são necessários para a aplicação atingir 300 mil usuários considerando que no lançamento da aplicação o número de usuários era nulo.

Para encontrar o número de meses necessários para a aplicação atingir 300 mil usuários, precisamos resolver a equação $500e^{0.1t} = 300$ para $t$. Isso nos dá:

$$
500e^{0.1t} = 300
$$

Dividindo ambos os lados por 500, obtemos:

$$
e^{0.1t} = \frac{300}{500}
$$

Aplicando o logaritmo natural de ambos os lados, obtemos:

$$
0.1t = \ln\left(\frac{300}{500}\right)
$$

Finalmente, resolvendo para $$t$$, obtemos:

$$
t = \frac{\ln(300/500)}{0.1} \approx 13.86 \, \text{meses}
$$

# Problema 2 – Otimizando o Tempo de Resposta de uma Aplicação Web

Suponha que você seja um desenvolvedor de uma aplicação web e esteja encarregado de otimizar o tempo de resposta de uma funcionalidade de pesquisa. Atualmente, o tempo de resposta médio para uma pesquisa é modelado pela função $f(t) = 0.1t^2 + 0.5t + 2$, onde $t$ é o tempo decorrido desde o início da pesquisa em segundos.

A integral definida de $f(t)$ em um intervalo [a, b] fornece o tempo total gasto na sessão de pesquisa. Por exemplo, se calcularmos a integral definida de $f(t)$ entre 0 e 10 segundos, obteremos o tempo total gasto pelos usuários durante o período específico. Isto nos permite comparar diferentes intervalos de tempos e identificar quais parte da sessão de pesquisa estão contribuindo mais para o tempo total de resposta.

## a) Calcule a integral definida de $f(t)$ nos primeiros 2s iniciais da pesquisa.

Para calcular a integral definida de $f(t)$ nos primeiros 2 segundos, vamos integrar $f(t)$ de 0 a 2 segundos:

$$
\int_{0}^{2} (0.1t^2 + 0.5t + 2) \, dt
$$

Integrando termo a termo, obtemos:

$$
= \left[ \frac{0.1}{3}t^3 + \frac{0.5}{2}t^2 + 2t \right]_{0}^{2}
$$
$$
= \left[ \frac{0.1}{3}(2)^3 + \frac{0.5}{2}(2)^2 + 2(2) \right] - \left[ \frac{0.1}{3}(0)^3 + \frac{0.5}{2}(0)^2 + 2(0) \right]
$$
$$
= \left[ \frac{0.1}{3}(8) + \frac{0.5}{2}(4) + 4 \right] - 0
$$
$$
= \left[ \frac{8}{30} + \frac{2}{2} + 4 \right]
$$
$$
= \left[ \frac{8}{30} + 1 + 4 \right]
$$
$$
= \frac{8}{30} + 1 + 4
$$
$$
= \frac{8}{30} + \frac{30}{30} + \frac{120}{30}
$$
$$
= \frac{158}{30} \approx 5.27 \, \text{segundos}
$$

## b) Calcule a integral definida de $f(t)$ entre o intervalo de tempo de 2s a 4s.

Agora, para calcular a integral definida de $f(t)$ entre 2 segundos e 4 segundos:

$$
\int_{2}^{4} (0.1t^2 + 0.5t + 2) \, dt
$$

Integrando novamente termo a termo:

$$
= \left[ \frac{0.1}{3}t^3 + \frac{0.5}{2}t^2 + 2t \right]_{2}^{4}
$$
$$
= \left[ \frac{0.1}{3}(4)^3 + \frac{0.5}{2}(4)^2 + 2(4) \right] - \left[ \frac{0.1}{3}(2)^3 + \frac{0.5}{2}(2)^2 + 2(2) \right]
$$
$$
= \left[ \frac{0.1}{3}(64) + \frac{0.5}{2}(16) + 8 \right] - \left[ \frac{0.1}{3}(8) + \frac{0.5}{2}(4) + 4 \right]
$$
$$
= \left[ \frac{6.4}{3} + \frac{8}{2} + 8 \right] - \left[ \frac{0.8}{3} + 2 + 4 \right]
$$
$$
= \left[ \frac{6.4}{3} + 4 + 8 \right] - \left[ \frac{0.8}{3} + 6 \right]
$$
$$
= \frac{6.4}{3} + 12 - \frac{0.8}{3} - 6
$$
$$
= \frac{6.4}{3} - \frac{0.8}{3} + 12 - 6
$$
$$
= \frac{6.4 - 0.8}{3} + 6
$$
$$
= \frac{5.6}{3} + 6
$$
$$
= \frac{5.6}{3} + \frac{18}{3}
$$
$$
= \frac{23.6}{3} \approx 7.87 \, \text{segundos}
$$

## c) Calcule a taxa de crescimento (em porcentagem) do tempo total de pesquisa considerando os primeiros 2s da pesquisa e depois o segundo 2s de pesquisa.

A taxa de crescimento do tempo total de pesquisa pode ser calculada comparando os tempos totais gastos nos primeiros 2 segundos e nos segundos 2 segundos de pesquisa. 

A taxa de crescimento é dada por:

$$
\text{Taxa de crescimento} = \left( \frac{\text{Tempo total nos segundos 2}}{\text{Tempo total nos primeiros 2}} - 1 \right) \times 100\%
$$

Substituindo os valores:

$$
\text{Taxa de crescimento} = \left( \frac{7.87}{5.27} - 1 \right) \times 100\%
$$
$$
= \left( \frac{7.87 - 5.27}{5.27} \right) \times 100\%
$$
$$
= \left( \frac{2.6}{5.27} \right) \times 100\%
$$

Agora, vamos calcular o valor numérico:

$$
= 49.34\%
$$

Portanto, a taxa de crescimento do tempo total de pesquisa, considerando os primeiros 2 segundos da pesquisa e depois o segundo 2 segundos de pesquisa, é de aproximadamente **49.34%**.
