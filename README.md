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
