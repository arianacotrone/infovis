# 💓 El pulso del movimiento (Ingeniería de Datos Personales)

Este repositorio contiene la entrega final para la materia de **Visualización de Datos (2026)**. El proyecto consiste en un dashboard web interactivo que analiza poco más de un año de actividad física personal, buscando entender la consistencia, las anomalías, el balance de las disciplinas y la optimización del rendimiento metabólico.

La aplicación cruza registros manuales de asistencia a entrenamientos con las métricas de salud automatizadas recopiladas por el **Apple Watch**.

🔗 **Puedes ver el Dashboard interactivo en vivo aquí:** [https://arianacotrone.github.io/infovis/tp-individual/index.html]

---

## 📊 Estructura del Dashboard y Preguntas de Negocio

El sitio web está organizado de forma narrativa a través de 5 secciones principales:

### 1. ¿Hay cierta intensidad estacional?
* **Visualización:** Mapa de calor interactivo (vía *Flourish*) + Gráfico *Beeswarm Plot* integrado como imagen (`actividad semanal.png`).
* **Insight:** Evidencia la densidad del entrenamiento semanal. Expone anomalías lógicas como las vacaciones en junio 2025 o bajas de densidad debido al crudo invierno, demostrando que la regularidad base se sostiene en la mayor parte del año entre 1 y 3 días semanales.

### 2. ¿Cómo se equilibra la actividad?
* **Visualización:** Gráfico de flujo estacional / áreas (vía *Flourish*).
* **Insight:** Muestra la correlación de compensación entre disciplinas; cuando la frecuencia de partidos de fútbol cae, las sesiones de gimnasio ganan un protagonismo estratégico.

### 3. ¿Cómo se estructura la semana?
* **Visualización:** Gráfico de distribución de actividades semanales (vía *Tableau Public*).
* **Insight:** Revela los hábitos cronológicos. Los lunes se aprovecha la mañana por un esquema laboral vespertino, mientras que los domingos se consolidan fuertemente como el día más elegido para jugar partidos.

### 4. ¿En qué días de la semana se concentra cada actividad?
* **Visualización:** Dos gráficos de torta / componentes distribuidos en paralelo (vía *Datawrapper*).
* **Insight:** Comparativa directa que demuestra la naturaleza de las agendas: el gimnasio se concentra con fuerza durante los días hábiles, mientras que el deporte (fútbol) se adueña de los fines de semana.

### 5. ¿Se evidencian cambios?
* **Visualización:** Gráfico de series temporales de variables fisiológicas (vía *Tableau Public*) con una sección interactiva de notas técnicas.
* **Insights Clave Analizados:**
  * **Ruido en la captura:** Huecos y anomalías debido a la fricción del agua en la pileta en días de natación interfiriendo con el sensor del Apple Watch.
  * **Respuesta Hemodinámica:** Elevación de pulsaciones promedio ligada a la recuperación fisiológica post-donación de sangre en marzo 2026 (Semana 61).
  * **Eficiencia Metabólica:** Caída de 0,8 puntos en el consumo calórico hacia fines de 2025 ante un esfuerzo similar (BPM constantes), indicando una mejora cardiopulmonar alegable al inicio de entrenamientos de resistencia.

---

## 🛠️ Tecnologías e Integraciones Utilizadas

Para lograr un diseño minimalista, editorial y fluido, se emplearon las siguientes herramientas:

* **Estructura y Estilos:** HTML5 semántico y CSS3 personalizado usando fuentes modernas (*Quicksand* y *Lora*) con transiciones animadas dinámicas activadas por el desplazamiento (`IntersectionObserver`).
* **Integración de Dashboards No-Code / Low-Code:**
  * **Flourish:** Para los gráficos de densidad y flujos interactivos.
  * **Tableau Public:** Inserción asincrónica mediante API (`viz_v1.js`) con cálculo automático de proporciones dinámicas de aspecto de los contenedores.
  * **Datawrapper:** Embebido mediante `iframes` responsivos con comunicación de eventos de altura de ventana mediante scripts.

