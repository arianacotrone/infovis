# 📊 Visualización de Información: Análisis de Entrenamientos y Métricas de Salud (Apple Watch)

Este repositorio contiene el proyecto final para la materia **Visualización de Información** de la **Maestría en Ciencia de Datos (ITBA)**. 

El objetivo del proyecto es explorar, mediante visualizaciones interactivas en la web, el impacto físico de mis entrenamientos diarios (Fútbol, Gimnasio y Tenis) registrados de forma manual, cruzándolos con las métricas de salud automatizadas que recopila mi **Apple Watch** a lo largo del año 2024.

---

## 🎯 Objetivos del Análisis

El dashboard busca responder a tres preguntas fundamentales a través de la exploración visual:
1. **Gasto Energético:** ¿Cómo varía el gasto calórico activo promedio según el tipo de actividad física y el día de la semana?
2. **Esfuerzo Cardiovascular:** ¿Qué disciplinas demandan una mayor frecuencia cardíaca máxima y promedio?
3. **Impacto en el Descanso:** ¿Existe alguna relación visible entre los días de entrenamiento intenso y la duración o eficiencia del sueño posterior?

---

## 🛠️ Tecnologías Utilizadas

El proyecto está construido íntegramente del lado del cliente como una aplicación web estática, utilizando las siguientes herramientas:
* **HTML5 y CSS3** para la estructura y el diseño de la interfaz.
* **Bootstrap 5** para lograr una maquetación limpia, moderna y un diseño responsivo.
* **D3.js (v7)** para la manipulación del DOM basada en datos y la creación de los gráficos dinámicos e interactivos.
* **JavaScript (ES6+)** para la lógica de carga, filtrado y procesamiento de los datasets en formato CSV.

---

## 📊 Visualizaciones Incluidas

El dashboard interactivo cuenta con tres secciones principales coordinadas entre sí:
* **Gráfico de Barras Agrupadas / Apiladas:** Muestra la distribución del gasto calórico por tipo de entrenamiento y días de la semana.
* **Gráfico de Dispersión (Scatter Plot):** Correlaciona la frecuencia cardíaca promedio vs. la máxima, permitiendo identificar la intensidad por disciplina mediante canales de color.
* **Línea de Tiempo / Mapa de Calor:** Permite observar los patrones de sueño (horas de descanso) al contrastar los días con actividad física frente a los días de sedentarismo.

---

## 📂 Estructura del Repositorio

```text
├── css/
│   └── styles.css          # Estilos personalizados y paleta de colores
├── data/
│   ├── entrenamientos.csv  # Registro manual de Fútbol, Gimnasio y Tenis (2024)
│   └── apple_watch.csv     # Métricas de salud (Calorías, FC, Sueño) exportadas
├── js/
│   ├── main.js             # Lógica general y carga de datos comunes
│   ├── barras.js           # Implementación del gráfico de gasto calórico en D3
│   ├── scatter.js          # Implementación del gráfico de frecuencia cardíaca
│   └── sueno.js            # Implementación de la visualización de descanso
├── index.html              # Estructura del Dashboard e integración con Bootstrap
└── README.md               # Documentación del proyecto
