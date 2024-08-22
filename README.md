import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Carregar dados (simulação de carregamento, ajuste conforme necessário)
# Exemplo: df = pd.read_csv('caminho/para/arquivo.csv')
# Para dados reais, você pode usar fontes como o ISP-RJ ou outras bases de dados públicas

# Simulação de dados
# Substitua este trecho pelo carregamento real dos dados
dates = pd.date_range(start='2010-01-01', end='2023-12-31', freq='M')
crime_rates = np.random.randint(1000, 5000, len(dates))
df = pd.DataFrame({'Date': dates, 'Crime Rate': crime_rates})
df.set_index('Date', inplace=True)

# Análise Estatística
print(df.describe())

# Visualização de Dados
plt.figure(figsize=(14, 7))
plt.plot(df['Crime Rate'], label='Taxa de Criminalidade', color='red')
plt.title('Taxa de Criminalidade no Rio de Janeiro (2010-2023)')
plt.xlabel('Data')
plt.ylabel('Número de Incidentes')
plt.legend()
plt.grid(True)
plt.show()

# Conclusão
print("Conclusão: A análise revela tendências simuladas na taxa de criminalidade ao longo do tempo.")
