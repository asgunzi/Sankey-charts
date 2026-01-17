# Data Visualization - Gráfico Sankey 

Sankey Charts são gráficos bonitos como o da figura abaixo.

Os nós são as barras verticais, e os links são as ligações entre os nós. É possível controlar praticamente tudo ao gerar o gráfico. Vamos ver alguns exemplos, em Python, biblioteca plotly.graph_objects.

![](.\newplot.png)

## Para entender o código

Primeiro, iniciamos com uma definição dos nós, mais especificamente, dos labels destes.

```python
node=dict(
        label=["Início", "Grupo A", "Grupo B", "Passou", "Não Passou"]
    )
```

A seguir, os links. O "source" é da onde começa, e o "target" onde o link termina. Os números 0, 1, 2, ... correspondem à mesma ordem definida no dicionários dos nós acima.

Portanto, um source de 0 para um target de 1 significa um link de "Início" para "Grupo A", no nosso exemplo.

```python
link=dict(
        source=[0, 0, 1, 2, 2],
        target=[1, 2, 3, 3, 4],
        value=[100, 50, 70, 80, 20]
)
```

Por fim, o value indica o tamanho do link. Não é necessário somar 100%

## Outras personalizações

É possível personalizar quase tudo no gráfico.

Por exemplo, dá para mudar as cores de cada nó, com uma lista de cores personalizadas.

```python
node=dict(
        label=["Início", "Grupo A", "Grupo B", "Passou", "Não Passou"]
        color=["blue", "green", "green", "orange", "red"]
    )
```

Ou dá para especificar manualmente a posição (x,y) de cada nó. 

```python
x=[0.0, 0.3, 0.3, 0.8],   # posição horizontal
y=[0.5, 0.2, 0.8, 0.5]   # posição vertical
```

![](.\newplot2.png)

As possibilidades são ilimitadas.

Divirta-se com o gráfico Sankey!

Documentação: [https://plotly.com/python/sankey-diagram/](https://plotly.com/python/sankey-diagram/)

Notebook disponível no Github [https://github.com/asgunzi/Sankey-charts](https://github.com/asgunzi/Sankey-charts)

