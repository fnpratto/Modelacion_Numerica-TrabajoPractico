
# Modelacion Numerica - TrabajoPractico (Simulación de Inundación en un Sótano)

Este proyecto aborda la simulación de inundación en un sótano debido a precipitaciones intensas, con un enfoque en la modelación numérica del sistema utilizando métodos de discretización. Se implementan varias técnicas numéricas para analizar el comportamiento del sistema bajo diferentes condiciones de precipitación y caudal de salida, así como para dimensionar la bomba de desagüe del sótano.

## Objetivos del Proyecto

El proyecto se centra en los siguientes objetivos:

### A) Modelación del Sistema

1. **Discretización de la Ecuación 1 con el Método de Euler:**
   - **Condiciones:** Se asume un coeficiente 𝐶 = 1 y un caudal de salida 𝑄ₛₐₗ = 0.
   - **Simulación:** Se corre el modelo para una precipitación de 60 minutos, verificando que el volumen de agua almacenado en el sótano coincida con el volumen de lluvia.

2. **Discretización de las Ecuaciones 1 y 6 con el Método de Euler:**
   - **Condiciones:** Se consideran 𝐶 y 𝑄ₛₐₗ como variables.
   - **Simulación:** Se corre el modelo para todas las duraciones e intensidades de precipitación, extendiendo el tiempo de simulación hasta que el sótano se vacíe.

### B) Dimensionamiento de la Bomba

- **Objetivo:** Redimensionar la bomba para adoptar un nuevo caudal máximo (𝑄ₘₐₓ) que garantice que la altura de agua en el sótano no exceda los 0,25 m para ninguna de las precipitaciones especificadas.

### C) Experimentación con Distintos Esquemas

1. **Discretización con el Método de Runge-Kutta de Orden 2:**
   - **Objetivo:** Considerar esta solución como "exacta".
   - **Simulación:** Se corre el modelo para una precipitación de 60 minutos.

2. **Comparación con el Método de Euler:**
   - **Condiciones:** Se realiza la simulación con Euler utilizando dos pasos de tiempo distintos.
   - **Verificación:** Se verifica que Euler es de orden 1 analizando la diferencia con la solución "exacta". Se utiliza el 𝑄ₘₐₓ obtenido en el punto B.

## Tecnologías Utilizadas

- **Python**: Lenguaje de programación utilizado para la implementación de la simulación.
- **Matplotlib**: Biblioteca de Python utilizada para la visualización de los resultados obtenidos en las simulaciones.
- **Google Colab**: Plataforma utilizada para ejecutar el código y permitir la experimentación interactiva con diferentes esquemas numéricos y parámetros del sistema.

## Ejecución en Google Colab

Puedes ejecutar este proyecto en Google Colab utilizando el siguiente enlace: [Simulación en Google Colab](https://colab.research.google.com/drive/1aegS0eFpOK4E1TY_k5fdbX6qLO1V0hfn?usp=sharing#scrollTo=DrWLKsR67_bZ).


## Visualización

La simulación produce un gráfico que muestra cómo evoluciona el volumen de agua en el sótano a lo largo del tiempo. Esto permite analizar visualmente el impacto de diferentes intensidades de lluvia y otros parámetros en la inundación del sótano.