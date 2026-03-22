# 📊 Arquivo Base - Assinaturas

Este repositório contém dados de assinaturas e passes de jogos, organizados em uma planilha Excel. O objetivo é demonstrar cálculos de valores totais utilizando fórmulas e funções do Excel.

## 📂 Estrutura dos Dados

![Gráfico de Assinaturas](https://github.com/AureliobotIA/TOTVS---Fundamentos-de-Engenharia-de-Dados-e-Machine-Learning/blob/main/Desafio%20-%20Criando%20um%20Dashboard%20de%20Vendas%20do%20Xbox%20com%20Excel/input/DashBoard%20Copilot%20Base%20Dados.JPG)

A planilha inclui as seguintes colunas:

- **Subscription Price**: Valor da assinatura principal (mensal, trimestral ou anual).
- **Subscription Type**: Tipo de assinatura.
- **EA Play Season Pass**: Indica se o passe está ativo.
- **EA Play Season Pass Price**: Valor do passe EA Play.
- **Minecraft Season Pass**: Indica se o passe está ativo.
- **Minecraft Season Pass Price**: Valor do passe Minecraft.
- **Coupon Val**: Valor de desconto aplicado.
- **Total Val**: Soma de todos os valores (assinatura + passes – cupom).

## 🧮 Fórmulas Utilizadas

O cálculo do **Total Val** é feito pela soma dos valores individuais:

\[
\text{Total} = \text{Subscription Price} + \text{EA Play Season Pass Price} + \text{Minecraft Season Pass Price} - \text{Coupon Val}
\]

Exemplo em Excel:

```excel
=SUM(A2:D2) - E2
🚀 Objetivo
•	Demonstrar uso de funções de soma no Excel.
•	Consolidar dados de diferentes tipos de assinaturas.
•	Criar uma base para análises futuras (ex.: comparação de planos, impacto de cupons).
📌 Como Usar
1.	Abra o arquivo Arquivo Base.xlsx.
2.	Explore os dados de cada linha.
3.	Verifique os cálculos na coluna Total Val.
4.	Ajuste valores de passes ou cupons para simular diferentes cenários.
📜 Licença
Este projeto é apenas para fins educacionais e não possui vínculo oficial com EA Play ou Minecraft.

---


# 📊 Arquivo Base - Análise de Assinaturas

Este repositório foi desenvolvido como parte de um projeto acadêmico, com o objetivo de consolidar e analisar dados de assinaturas de serviços digitais. O material serve como estudo de caso para aplicação de conceitos de organização de dados, uso de planilhas eletrônicas e funções de cálculo.

## 🎯 Objetivos do Projeto

- Demonstrar a aplicação de funções matemáticas em planilhas (ex.: `SUM`).
- Estruturar dados de diferentes tipos de assinaturas e passes.
- Explorar cenários de descontos e valores totais.
- Servir como base para futuras análises comparativas entre planos.

## 📂 Estrutura dos Dados

A planilha **Arquivo Base.xlsx** contém as seguintes variáveis:

- **Subscription Price**: Valor da assinatura principal.
- **Subscription Type**: Tipo de assinatura (Mensal, Trimestral, Anual).
- **EA Play Season Pass**: Indicação de ativação do passe.
- **EA Play Season Pass Price**: Valor do passe EA Play.
- **Minecraft Season Pass**: Indicação de ativação do passe.
- **Minecraft Season Pass Price**: Valor do passe Minecraft.
- **Coupon Val**: Valor de desconto aplicado.
- **Total Val**: Resultado da soma dos valores, considerando descontos.

## 🧮 Metodologia de Cálculo

O valor total é obtido pela seguinte fórmula:

\[
\text{Total Val} = \text{Subscription Price} + \text{EA Play Season Pass Price} + \text{Minecraft Season Pass Price} - \text{Coupon Val}
\]

No Excel, a função utilizada é:

```excel
=SUM(A2:D2) - E2
📌 Procedimentos
1.	Abrir a planilha Arquivo Base.xlsx.
2.	Identificar os valores de cada assinatura e passes.
3.	Observar os cálculos automáticos na coluna Total Val.
4.	Alterar valores de passes ou cupons para simular diferentes cenários.
📜 Considerações Finais
Este repositório exemplifica a importância da organização de dados e da aplicação de funções matemáticas em planilhas eletrônicas. O estudo contribui para a compreensão de como pequenas variações (como cupons de desconto) podem impactar o valor final de serviços digitais.
________________________________________


## 📈 Análises Complementares


![Gráfico de Assinaturas](https://github.com/AureliobotIA/TOTVS---Fundamentos-de-Engenharia-de-Dados-e-Machine-Learning/blob/main/Desafio%20-%20Criando%20um%20Dashboard%20de%20Vendas%20do%20Xbox%20com%20Excel/input/DashBoard%20Copilot.JPG)

Além dos cálculos básicos, foram gerados gráficos para melhor visualização dos dados:

- **Distribuição por Tipo de Assinatura**: mostra a proporção entre planos Mensais, Trimestrais e Anuais.
- **Impacto dos Cupons de Desconto**: compara valores totais com e sem aplicação de cupons.
- **Valor Médio por Passe de Jogo**: evidencia a diferença de custo entre EA Play e Minecraft.

### Exemplos de Gráficos

1. **Gráfico de Barras - Tipos de Assinatura**
   - Eixo X: Tipos de assinatura
   - Eixo Y: Quantidade de registros

2. **Gráfico de Pizza - Participação dos Cupons**
   - Percentual de assinaturas que tiveram desconto aplicado.

3. **Gráfico de Linhas - Evolução do Valor Total**
   - Mostra como o valor final varia conforme a combinação de passes e cupons.

---

## 🔎 Discussão

Os gráficos permitem observar que:
- Assinaturas **anuais** tendem a concentrar maior valor agregado.
- O uso de **cupons** tem impacto significativo na redução do valor final.
- O passe **Minecraft** aparece com maior frequência em relação ao EA Play, sugerindo preferência dos usuários.

---
👉 Você pode gerar esses gráficos direto no Excel (Inserir → Gráfico) ou, se quiser impressionar ainda mais, criar um notebook em Python usando bibliotecas como pandas e matplotlib para ler a planilha e gerar visualizações automaticamente.

Aqui vai um modelo inicial:
# análise_assinaturas.py

import pandas as pd
import matplotlib.pyplot as plt

# 1. Carregar a planilha
df = pd.read_excel("Arquivo Base.xlsx")

# 2. Distribuição por tipo de assinatura
assinaturas = df["Subscription Type"].value_counts()
assinaturas.plot(kind="bar", title="Distribuição por Tipo de Assinatura")
plt.xlabel("Tipo de Assinatura")
plt.ylabel("Quantidade")
plt.savefig("assinaturas_por_tipo.png")
plt.close()

# 3. Impacto dos cupons
df["Com Cupom"] = df["Coupon Val"] > 0
cupons = df["Com Cupom"].value_counts()
cupons.plot(kind="pie", autopct="%1.1f%%", title="Impacto dos Cupons")
plt.savefig("impacto_cupons.png")
plt.close()

# 4. Valor médio por passe
passes = {
    "EA Play": df["EA Play Season Pass Price"].mean(),
    "Minecraft": df["Minecraft Season Pass Price"].mean()
}
pd.Series(passes).plot(kind="bar", title="Valor Médio por Passe")
plt.ylabel("Valor Médio (R$)")
plt.savefig("valor_medio_passes.png")
plt.close()

print("Gráficos gerados com sucesso!")
O que esse script faz:
•	Lê sua planilha Arquivo Base.xlsx.
•	Cria 3 gráficos: 
o	Distribuição dos tipos de assinatura (barras).
o	Percentual de assinaturas com cupons (pizza).
o	Valor médio dos passes EA Play e Minecraft (barras).
•	Salva os gráficos como imagens (.png) para você incluir no repositório.



# 📊 Análise de Assinaturas

Este notebook complementa o repositório com análises gráficas e explicações passo a passo.

---

## 1. Importação de Bibliotecas
```python
import pandas as pd
import matplotlib.pyplot as plt
2. Carregamento dos Dados
df = pd.read_excel("Arquivo Base.xlsx")
df.head()
3. Distribuição por Tipo de Assinatura
df["Subscription Type"].value_counts().plot(kind="bar")
plt.title("Distribuição por Tipo de Assinatura")
plt.show()
4. Impacto dos Cupons
df["Com Cupom"] = df["Coupon Val"] > 0
df["Com Cupom"].value_counts().plot(kind="pie", autopct="%1.1f%%")
plt.title("Impacto dos Cupons")
plt.show()
5. Valor Médio por Passe
passes = {
    "EA Play": df["EA Play Season Pass Price"].mean(),
    "Minecraft": df["Minecraft Season Pass Price"].mean()
}
pd.Series(passes).plot(kind="bar")
plt.title("Valor Médio por Passe")
plt.ylabel("Valor Médio (R$)")
plt.show()
________________________________________
📌 Conclusão
Os gráficos mostram padrões importantes, como a predominância de assinaturas anuais e o impacto dos cupons na redução do valor final.

Esse notebook pode ser salvo como `analise_assinaturas.ipynb` e incluído no repositório junto com o README e a planilha. Assim, você entrega um pacote completo: **dados + documentação + análise prática**.  

