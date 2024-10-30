# Projects-Colab

# 📊 Projeto de Gráfico de Pizza com Python e Matplotlib

Este projeto cria um gráfico de pizza colorido utilizando a biblioteca `matplotlib` em Python! O gráfico exibe a distribuição de alunos por diferentes escolas e creches, e mostra as porcentagens em cada fatia de maneira estilosa 🎨.

## 🚀 Tecnologias Utilizadas

- **Python** 🐍
- **Matplotlib** 📈

## 📋 Funcionalidades

- Gráfico de pizza colorido e personalizado.
- Exibe porcentagens em cada fatia 🍰.
- Destaque com cores e sombra para melhor visualização.

## 📄 Código

O código abaixo configura as fatias do gráfico, seus rótulos, cores e também formata o texto das porcentagens para aparecer em branco:

```python
import matplotlib.pyplot as plt

# Dados
fatias = [540, 475, 560, 280, 613, 125, 140, 90, 50]
alunos = ['Luiz De Oliveira', 'Calil Miguel Allem', 'José Antonio Francisco', 'Barão De Santo Ângelo', 
          'Diogo Penha', 'Estrelinha Do Mar', 'Peixinho Dourado', 'Golfinho Do Mar', 'Abelinha']
divisao = ['yellow', 'orange', 'blue', 'green', 'gray', 'pink', 'gold', 'purple', 'brown']

# Função para definir a cor das porcentagens como branca
def make_autopct(pct):
    return f'{pct:.1f}%'

# Exibindo o gráfico de pizza com porcentagens em branco
plt.pie(fatias, labels=alunos, colors=divisao, startangle=90, shadow=True, 
        explode=(0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.1),
        autopct=lambda pct: plt.text(0, 0, make_autopct(pct), color='white', ha='center', va='center')) 

plt.title('Alunos por escolas e creches')
plt.show()
