# 📊 Educational Data Analytics Web App

### Descripción

Aplicación web interactiva desarrollada para explorar y visualizar datos educativos mediante dashboards dinámicos e intuitivos.

El proyecto fue diseñado para facilitar el análisis exploratorio de datos (EDA), permitiendo identificar patrones, tendencias y relaciones entre variables a través de visualizaciones interactivas.

### 🎯 Objetivos

* Explorar conjuntos de datos mediante análisis visual.
* Facilitar la identificación de tendencias y comportamientos.
* Crear una experiencia intuitiva para la exploración de datos.
* Desplegar una solución web accesible desde cualquier dispositivo.

### 🛠️ Tecnologías Utilizadas

* Python
* Pandas
* Streamlit
* Plotly Express
* Render

### 📈 Funcionalidades

✅ Dashboard interactivo

✅ Histogramas dinámicos para analizar distribuciones de variables

✅ Gráficos de dispersión para identificar correlaciones

✅ Visualizaciones interactivas con Plotly

✅ Interfaz web desarrollada con Streamlit

✅ Despliegue en la nube mediante Render

### 🚀 Resultados

El proyecto demuestra la integración de análisis de datos, visualización interactiva y desarrollo web para transformar conjuntos de datos en información útil para la toma de decisiones.


---

## Funcionalidades do Aplicativo Web

No aplicativo que desenvolvi, implementei:

1. Um **cabeçalho** para apresentar o projeto ao usuário.  
2. Um **histograma interativo**, gerado ao clicar em um botão ou selecionar uma caixa de seleção, para analisar distribuições de variáveis como odômetro, preço ou ano do veículo.  
3. Um **gráfico de dispersão interativo**, também acionado por botão ou caixa de seleção, permitindo observar relações entre diferentes variáveis do dataset.  
4. Integração com **Plotly Express** para gráficos interativos e responsivos.  
5. Um layout simples, funcional e fácil de usar.

Exemplo de trecho de código utilizado:

```python
import pandas as pd
import plotly.express as px
import streamlit as st

# Leitura do dataset
car_data = pd.read_csv('vehicles_us.csv')

# Criar um botão para histograma
hist_button = st.button('Criar histograma')
if hist_button:
    st.write('Criando um histograma para o conjunto de dados de anúncios de carros')
    fig = px.histogram(car_data, x="odometer")
    st.plotly_chart(fig, use_container_width=True)

# Criar um botão para gráfico de dispersão
scatter_button = st.button('Criar gráfico de dispersão')
if scatter_button:
    st.write('Criando gráfico de dispersão para análise exploratória')
    fig = px.scatter(car_data, x="odometer", y="price")
    st.plotly_chart(fig, use_container_width=True)
