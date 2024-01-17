# Proyecto de Verificación de Edad en Supermercados Good Seed

## Propósito del Proyecto

La cadena de supermercados Good Seed busca utilizar la ciencia de datos para cumplir con las leyes sobre la venta de alcohol, asegurándose de no vender alcohol a personas menores de edad. Para lograr esto, se propone construir y evaluar modelos de redes neuronales con arquitectura ResNet50, que utilicen métodos de visión artificial para determinar la edad de una persona a partir de una foto. El objetivo es alcanzar una métrica de Error Absoluto Medio (EAM) inferior a 7.

## Inicialización

Se importan las bibliotecas necesarias, incluyendo TensorFlow, y se definen las funciones y configuraciones iniciales.

## Carga de Datos

Se carga el conjunto de datos desde la carpeta /datasets/faces/. Los datos constan de 7591 imágenes con etiquetas de edades en el archivo labels.csv. Se utiliza un generador ImageDataGenerator para gestionar la carga eficiente de las imágenes.

## Exploración de Datos (EDA)

Se realiza una exploración de los datos, incluyendo estadísticas descriptivas, un histograma y un diagrama de cajas para comprender la distribución de las edades en el conjunto de datos. Se observa que el rango de edades es de 1 a 100 años, con una concentración en el rango de 20 a 40 años.

## Modelado

Se definen funciones para cargar conjuntos de entrenamiento y prueba, crear el modelo ResNet50, y entrenar el modelo. Se proponen tres modelos diferentes, cada uno con variaciones en la arquitectura y técnicas de aumento de datos.

## Preparación del Script para GPU

Se prepara un script para ejecutar el modelo en una plataforma GPU, exportando las funciones y configuraciones necesarias.

## Resultados de Modelos

Se muestran los resultados y gráficos de los modelos 1, 2 y 3. El modelo 1 presenta un EAM en el conjunto de validación de 6.03, pero muestra sobreajuste. El modelo 2 mejora el sobreajuste al incluir capas Dropout y un aumento de datos, alcanzando un EAM de 5.84 en validación. El modelo 3, con más capas y aumentos, logra un EAM de 5.85 en validación.

## Conclusiones

Se concluye que los modelos presentan mejoras al incluir capas Dropout y aumentos de datos. Sin embargo, se observa que modelos con arquitecturas más complejas tienden a sobreajustarse. Se sugiere seguir explorando configuraciones y técnicas para mejorar el rendimiento del modelo en conjuntos de datos futuros.

## Estructura del Repositorio
- `src/`: Contiene los scripts y notebooks de código fuente utilizados para realizar el análisis y entrenar los modelos.
- `data/`: No fue posible subir los datos por la carga computacional que esta requería 
- `README.md`: Este archivo, que proporciona una guía detallada sobre el proyecto, sus objetivos y la estructura del repositorio.

