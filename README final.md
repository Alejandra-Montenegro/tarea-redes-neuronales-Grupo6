
# Sistema de Recomendación con Redes Neuronales desde Cero

Este proyecto implementa una red neuronal feedforward utilizando únicamente NumPy, con el objetivo de predecir valoraciones de usuarios en una plataforma de streaming. Forma parte del Proyecto 3 del curso de Inteligencia Artificial.

## Objetivos

- Implementar redes neuronales desde cero sin frameworks externos.
- Aplicar algoritmos de optimización como gradiente descendente y regla delta.
- Evaluar diferentes arquitecturas y funciones de activación.
- Comparar el rendimiento con modelos tradicionales como regresión lineal.

## Arquitectura del Modelo

- Entradas: Representación BoW de títulos y tags de películas.
- Capas ocultas: 2 capas densas con activaciones ReLU, Tanh y Sigmoid.
- Salida: Clasificación por década de lanzamiento.
- Funciones de activación disponibles: Sigmoid, ReLU, Tanh.
- Inicialización de pesos: Xavier y He.
- Optimización: Gradiente descendente manual.

## Hiperparámetros

- Épocas: 20
- Learning rate: 0.01, 0.05, 0.1 (según experimento)
- Batch size: 128

## Resultados

| Modelo                      | Accuracy Test |
|----------------------------|---------------|
| Red Neuronal (base)        | 0.9929        |
| Regresión Logística (sklearn) | 0.9936        |
| Softmax NumPy              | 0.9738        |

## Visualizaciones

- Curvas de entrenamiento (accuracy y pérdida).
- Matriz de confusión por década.
- Comparación de configuraciones en performance_comparison.csv.

## Experimentación

Se probaron múltiples configuraciones:
- Arquitecturas: pequeña (64-32), base (128-64), grande (256-128).
- Activaciones: ReLU, Tanh, Sigmoid.
- Inicializaciones: He, Xavier.
- Learning rates: 0.01, 0.05, 0.1.

## Aplicación adicional

Se incluye una red neuronal para predicción de ratings simulados entre usuarios y películas, comparada con regresión lineal.

## Limitaciones

- Implementación sin frameworks modernos limita la escalabilidad.
- No se incluye regularización ni entrenamiento por lotes dinámico.

## Futuras Mejoras

- Migración a TensorFlow o PyTorch.
- Uso de embeddings para usuarios e ítems.
- Entrenamiento en GPU.
- Incorporación de técnicas como dropout y batch normalization.

## Estructura del Notebook

- Carga y procesamiento de datos desde ZIP.
- Vectorización BoW.
- Implementación de red neuronal desde cero.
- Entrenamiento y evaluación.
- Comparación con modelos base.
- Experimentación con hiperparámetros.

## Grupo 6

- María Fernanda Aguirre Aguirre
- Sebastián Nicolas Diaz Ribadeneira
- Edgar Ricardo García Ortiz
- Alejandra Carolina Montenegro Fernández
- Yadira Emperatriz Paguay Méndez
- María Sol Vásquez Córdova
