# Projects-Colab

# 📊 Projeto de Visualização de Dados com Gráficos em Python

Este projeto foi desenvolvido para explorar a criação de gráficos em Python utilizando a biblioteca `Matplotlib`, em conjunto com `Pandas` e `NumPy`. A proposta incluiu a visualização de dados em diferentes formatos, como tabelas, gráficos de pizza, gráficos de linha e gráficos de dispersão.

## 🚀 Tecnologias Utilizadas

- **Python** 🐍
- **Pandas** 📑
- **NumPy** 🔢
- **Matplotlib** 📊

## 📋 Funcionalidades e Comandos

Este projeto é dividido em diversas seções, cada uma com comandos e funcionalidades específicas:

### 1️⃣ Exibir uma Série com a Quantidade de Alunos por Titulação

Foi criada uma série em `Pandas` para mostrar o número de alunos por diferentes níveis de titulação.

```python
import pandas as pd

Titulação = pd.Series(['Doutorado', 'Mestrado', 'Especialização', 'Graduação', 'Cursos Técnicos'],
                      index=[20, 15, 85, 145, 320])
print(Titulação)

2️⃣ Exibir uma Tabela com a Quantidade de Alunos por Titulação
Aqui, criamos um DataFrame para exibir a titulação e a quantidade de alunos em forma de tabela.
df = pd.DataFrame({'Titulação': ['Doutorado', 'Mestrado', 'Especialização', 'Graduação', 'Cursos Técnicos'],
                   'Quantidade': [20, 15, 85, 145, 320]})
print(df)

3️⃣ Exibir uma Tabela com Calorias e Percentual de Gordura de Alimentos
Um DataFrame para mostrar as calorias e o percentual de gordura de diferentes alimentos.
df = pd.DataFrame({'calorias': [200, 350, 550], 'gordura (%)': [0, 15, 35]},
                  index=['banana', 'macarrão', 'cachorro quente'])
print(df)

4️⃣ Criar uma Matriz 3D com NumPy
Usamos o NumPy para criar uma matriz 3D com 50 elementos, explorando as propriedades de shape, dimensões e número de elementos.
import numpy as np

v = np.array(range(50)).reshape(2, 5, 5)
print('Shape = ', v.shape)
print('Número de dimensões = ', v.ndim)
print('Número de elementos = ', v.size)
print('Tensor v = \n', v)

5️⃣ Criar um Gráfico de Pizza com Destaque e Porcentagens
Criamos um gráfico de pizza para representar o número de alunos em cada escola, incluindo porcentagens exibidas em branco para melhor visibilidade.
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
        autopct=lambda pct: make_autopct(pct), textprops={'color': 'white'}) 

plt.title('Alunos por escolas e creches')
plt.show()

6️⃣ Criar um Gráfico de Linha
Exibimos um gráfico de linha simples para representar relações entre duas variáveis.
x = [1, 3, 5]
y = [1, 2, 5]

plt.plot(x, y)
plt.title('Exemplo de Gráfico de Linha')
plt.xlabel('Variável 1')
plt.ylabel('Variável 2')
plt.plot(x, y, label='Uma legenda')
plt.legend()
plt.show()

7️⃣ Criar um Gráfico de Dispersão com Pontos em Forma de Estrela
Por fim, um gráfico de dispersão com pontos no formato de estrela para destacar a distribuição dos dados.

x = [1, 2, 3, 4, 5, 6, 7, 8]
y = [5, 2, 4, 5, 6, 8, 4, 8]

plt.scatter(x, y, label='Pontos', color='b', marker='*', s=100)
plt.legend()
plt.show()

📊 Visualizações
As visualizações criadas incluem:

Gráficos de Pizza com porcentagens em destaque.
Gráficos de Linha para visualização de dados sequenciais.
Gráficos de Dispersão para observar a distribuição de pontos em um plano cartesiano.
🔧 Como Executar o Projeto
1 Clone o repositório:
git clone https://github.com/seu-usuario/projeto-visualizacao-dados.git

2 Instale as bibliotecas necessárias:
pip install numpy pandas matplotlib

Execute o código em um ambiente Python (Google Colab, Jupyter Notebook ou IDE como PyCharm).

📚 Referências e Aprendizado
Este projeto é uma excelente introdução à manipulação de dados e visualização com Python, Pandas, NumPy e Matplotlib. 🧠

📝 Licença
Este projeto é de uso livre para estudos e prática. Compartilhe e contribua! 🌟

Feito com ❤️ e Python! 🚀

Esse README cobre todos os comandos e funcionalidades que você explorou, com instruções de uso e explicações de cada etapa.

