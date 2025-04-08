# RAMOS MAMANI CRISHMAN COM300 PRIMER PARCIAL
✅ Ventajas de usar una red neuronal en PyTorch

    Abstracción de bajo nivel + flexibilidad:

        Puedes definir arquitecturas complejas sin programar toda la retropropagación manualmente.

    Uso de GPU:

        PyTorch permite aprovechar aceleración por GPU fácilmente (.to(device)), lo que acelera mucho el entrenamiento.

    Optimización automática (autograd):

        No necesitas implementar el cálculo de gradientes manualmente; PyTorch lo hace con loss.backward().

    Integración con datasets e imágenes:

        Soporte directo para torchvision.datasets, transformaciones y loaders, ideal para imágenes.

    Depuración más sencilla:

        Puedes imprimir y monitorear estados internos fácilmente, incluso insertar puntos de interrupción.

⚠️ Desventajas (o retos) de usar PyTorch

    Curva de aprendizaje:

        Puede ser más complejo para principiantes que una implementación básica en NumPy.

    Menos control explícito:

        Si estás aprendiendo teoría, PyTorch te oculta detalles importantes como derivadas parciales o cómo fluye el gradiente.

    Dependencia de entorno:

        Requiere instalación de librerías y configuración adecuada del entorno, especialmente para GPU.

🔍 Diferencias clave con un algoritmo de clasificación con retropropagación "generalizado" (hecho desde cero)
Aspecto	PyTorch (como en tu código)	Implementación Generalizada (NumPy/Scipy)
Retropropagación	Automática (autograd)	Manual (tú calculas los gradientes)
Entrenamiento en GPU	Sí	No (solo CPU, más lento)
Escalabilidad	Alta	Limitada (difícil escalar a grandes datasets)
Modularidad	Alta (modelos, optimizadores, transformaciones)	Baja o manual
Facilidad para debugging educativo	Media	Alta (ves todo lo que ocurre)
🎓 ¿Cuándo usar cada uno?

    Para aprender conceptos: Mejor implementar desde cero con NumPy.

    Para aplicaciones reales: Mejor usar PyTorch por su eficiencia, comunidad y escalabilidad.
