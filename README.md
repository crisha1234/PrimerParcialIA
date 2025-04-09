# RAMOS CRISHMAN COM300 PRIMER PARCIAL
Comparación de Modelos de Clasificación: Numpy vs PyTorch

Este documento presenta una comparación entre dos enfoques para construir y entrenar una red neuronal de clasificación de imágenes. Los modelos se implementan utilizando Numpy (sin bibliotecas avanzadas) y PyTorch (una biblioteca de deep learning). A continuación, se detallan las diferencias clave entre ambos enfoques, sus ventajas y desventajas, y se determina cuál es la mejor alternativa según el contexto de uso.
1. Implementación y Estructura del Código
Numpy (Primer Código)

    Implementación Manual: Cada componente de la red neuronal (cálculo de activación, propagación hacia adelante, retropropagación, función de costo, optimización) se implementa manualmente.

    Optimización: Se utiliza optimize.minimize de SciPy para ajustar los pesos durante el proceso de retropropagación.

    Complejidad: El código es detallado, lo que permite entender cada componente de la red, pero también es propenso a errores y más largo.

PyTorch (Segundo Código)

    Abstracción del Proceso: PyTorch abstrae muchos de los detalles de la red neuronal. Se utilizan clases (nn.Module) para definir el modelo de manera concisa.

    Optimización Automática: PyTorch maneja la optimización automáticamente, utilizando optimizadores como AdamW.

    Manejo de Datos: El uso de DataLoader y transformaciones de torchvision facilita la carga y preprocesamiento de datos.

2. Optimización y Computación
Numpy (Primer Código)

    La optimización se realiza de manera manual, utilizando SciPy para minimizar la función de costo.

    El proceso de actualización de pesos también es manual, lo que puede ser menos eficiente y más propenso a errores.

    No optimiza el uso de hardware, por lo que no se aprovechan las ventajas de la aceleración por GPU.

PyTorch (Segundo Código)

    Optimización Automática: PyTorch tiene soporte nativo para optimización de gradientes, actualizando los pesos de manera eficiente.

    Soporte para GPU: PyTorch puede usar CUDA para entrenar el modelo en una GPU, acelerando el proceso de entrenamiento.

    Optimización Adaptativa: El uso de optimizadores avanzados como AdamW mejora el rendimiento durante el entrenamiento.

3. Manejo de Datos
Numpy (Primer Código)

    El proceso de carga y preprocesamiento de datos se realiza manualmente, lo que puede ser más tedioso y propenso a errores.

    No hay soporte directo para batches de datos, lo que significa que todo el conjunto de datos debe cargarse en memoria, lo que puede no ser ideal para datasets grandes.

PyTorch (Segundo Código)

    DataLoader: Facilita la carga de datos en batches, optimizando la memoria y acelerando el entrenamiento.

    Transformaciones: PyTorch permite realizar transformaciones como redimensionado y normalización de las imágenes de manera sencilla.

    División de Datos: Los datos se dividen automáticamente en entrenamiento y prueba usando random_split.

4. Facilidad de Uso y Extensibilidad
Numpy (Primer Código)

    El código es menos modular y requiere más esfuerzo manual para ajustar y modificar el modelo.

    Cambiar la arquitectura de la red o agregar nuevas capas implica modificar muchas partes del código.

PyTorch (Segundo Código)

    Modularidad: Definir el modelo en PyTorch usando clases nn.Module hace que el código sea más modular y reutilizable.

    Extensibilidad: PyTorch permite agregar nuevas capas, cambiar la arquitectura de la red (por ejemplo, agregar convoluciones o redes recurrentes) sin reescribir mucho código.

5. Rendimiento
Numpy (Primer Código)

    El rendimiento es más bajo, especialmente para datasets grandes. La optimización manual y la falta de soporte para GPU ralentizan el proceso de entrenamiento.

    No se aprovecha la aceleración de hardware, lo que aumenta el tiempo necesario para entrenar modelos complejos.

PyTorch (Segundo Código)

    El rendimiento es mucho más rápido y eficiente gracias al uso de optimización automática y el soporte para entrenamiento en GPU.

    PyTorch es más escalable y puede manejar datasets grandes de manera eficiente.

6. Resultados y Precisión
Numpy (Primer Código)

    El rendimiento en términos de precisión depende en gran medida de la correcta implementación de cada componente.

    Mayor riesgo de errores en la implementación manual, lo que puede afectar negativamente la precisión final.

PyTorch (Segundo Código)

    Mejores resultados en términos de precisión y eficiencia, ya que PyTorch optimiza automáticamente los cálculos y actualizaciones de pesos.

    Utiliza optimizadores avanzados y técnicas modernas que mejoran el rendimiento general del modelo.

Conclusión: ¿Cuál es la Mejor Alternativa?
PyTorch es la mejor alternativa para entrenar redes neuronales en proyectos reales, especialmente cuando el rendimiento y la escalabilidad son importantes. A pesar de que el enfoque basado en Numpy es útil para comprender los fundamentos de las redes neuronales, PyTorch ofrece varias ventajas:

    Optimización automática de gradientes.

    Soporte para GPU, acelerando drásticamente el entrenamiento.

    Facilidad de uso y extensibilidad, con un código más limpio y modular.

    Rendimiento superior al manejar grandes volúmenes de datos.

Por lo tanto, si tu objetivo es desarrollar modelos de producción y aprovechar la eficiencia computacional, PyTorch es la opción más adecuada.
