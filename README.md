# Atividade Avaliativa de Cálculos de Área

Este repositório é dedicado à atividade avaliativa de cálculos de área, correspondente à terceira semana da segunda sprint do módulo 2 do Inteli - Instituto de Tecnologia e Liderança. O foco desta atividade é a matemática e a física. Neste contexto, aceitamos o desafio de explorar como as integrais indefinidas e definidas podem ser aplicadas em problemas de aplicação web.

## Problema 1 – Modelagem do Crescimento de Usuários em uma Aplicação Web

### a) Com auxílio de software, faça o gráfico da função $f(t)$ para $t<30$.

Para fazer o gráfico da função $f(t) = 50e^{0.1t}$ para $t < 30$, você pode usar um software de plotagem gráfica como o Matplotlib em Python. Aqui está um exemplo de código que você pode usar para gerar o gráfico:

```python
import matplotlib.pyplot as plt
import numpy as np

t = np.linspace(0, 30, 100)
f_t = 50 * np.exp(0.1 * t)

plt.plot(t, f_t)
plt.title('Gráfico de $f(t) = 50e^{0.1t}$')
plt.xlabel('Tempo (meses)')
plt.ylabel('Taxa de crescimento (milhares de pessoas por mês)')
plt.grid(True)
plt.show()
```

![Gráfico de f(t)](graph.png)

### b) Determine o número de meses necessário para dobrar a taxa de crescimento inicial do número de usuários da aplicação web.

Para determinar o número de meses necessário para dobrar a taxa de crescimento inicial do número de usuários da aplicação web, precisamos resolver a equação $50e^{0.1t} = 2 * 50$ para $t$. Isso nos dá $t = \frac{\ln(2)}{0.1} \approx 6.93$ meses.

### c) Encontre a função $F(t)$. Discuta o significado da constante que aparecerá na integração indefinida. O que é necessário saber para definir o valor da constante?

A função $F(t)$ é a integral indefinida de $f(t)$. Portanto, $F(t) = \int f(t) dt = \int 50e^{0.1t} dt = 500e^{0.1t} + C$, onde $C$ é a constante de integração. O valor de $C$ depende das condições iniciais do problema. No nosso caso, como o número de usuários era nulo no lançamento da aplicação, temos $C = 0$.

### d) Quantos meses são necessários para a aplicação atingir 300 mil usuários considerando que no lançamento da aplicação o número de usuários era nulo.

Para encontrar o número de meses necessários para a aplicação atingir 300 mil usuários, precisamos resolver a equação $500e^{0.1t} = 300$ para $t$. Isso nos dá $t = \frac{\ln(300/500)}{0.1} \approx 13.86$ meses.

## Conclusão

Através desta atividade, pudemos explorar a aplicação prática do cálculo integral e diferencial na modelagem do crescimento de usuários em uma aplicação web. A matemática, e em particular o cálculo, fornece ferramentas poderosas que nos permitem entender e modelar fenômenos complexos no mundo real. Ao aplicar essas ferramentas, somos capazes de fazer previsões precisas e informadas que podem ajudar a orientar a tomada de decisões e otimizar o desempenho. Continuaremos a explorar essas aplicações em atividades futuras.
