# Clasificación de Dígitos con MNIST usando PyTorch

Este proyecto implementa una red neuronal simple para clasificar dígitos escritos a mano utilizando el dataset MNIST. Este dataset es un conjunto clásico para tareas de aprendizaje supervisado en clasificación de imágenes.

## Descripción del proyecto

La red neuronal construida tiene como objetivo aprender a clasificar imágenes de dígitos (del 0 al 9) en sus respectivas categorías. El modelo se entrena con PyTorch y utiliza una arquitectura de red neuronal feedforward.

### Características principales:
- **Dataset MNIST**: Imágenes en escala de grises de 28x28 píxeles.
- **Arquitectura del modelo**:
  - Entrada: 784 neuronas (28x28 píxeles aplanados).
  - Capas ocultas: Dos capas densas (128 y 64 neuronas) con activación ReLU.
  - Salida: 10 neuronas (una para cada clase del 0 al 9).
- **Optimizador**: Adam.
- **Función de pérdida**: Cross-Entropy Loss.

## Requisitos

Asegúrate de tener instaladas las siguientes dependencias:

- Python >= 3.7
- PyTorch
- torchvision
- matplotlib (opcional, para visualización)

Puedes instalar las dependencias usando pip:

```bash
pip install torch torchvision matplotlib
```

## Ejecución

### 1. Clona el repositorio o descarga el código fuente:

```bash
git clone https://github.com/GabrielDT13/Mnist.git
cd tu-repositorio
```

### 2. Ejecuta el script principal

### Entrenamiento
Ejecuta el código para entrenar el modelo. Durante el entrenamiento:
1. El modelo procesa las imágenes del directorio `train`.
2. Evalúa la precisión en las imágenes del directorio `test` después de cada epoch.

### 3. Visualiza los resultados

El modelo mostrará la pérdida por época y la precisión final en el conjunto de prueba. Además, puedes visualizar las predicciones del modelo para imágenes individuales.

## Estructura del proyecto

```
.
├── data/                  # Carpeta donde se descargará el dataset MNIST
├── minist.ipynb           # Script principal
```

## Ejemplo de uso

Aquí tienes un ejemplo de cómo el modelo predice un dígito:

```bash
Etiqueta real: 7
Predicción del modelo: 7
```

Y también puedes visualizar la imagen del dígito predicho:

```python
import matplotlib.pyplot as plt

# Mostrar imagen y predicción
plt.imshow(single_image.squeeze(0), cmap="gray")
plt.title(f"Predicción: {predicted_label.item()}")
plt.show()
```

## Mejoras futuras

- Implementar una red neuronal convolucional (CNN) para mejorar la precisión.
- Guardar y cargar modelos entrenados.
- Incorporar experimentos con hiperparámetros como el learning rate o el número de épocas.
- Visualizar las matrices de confusión para un análisis más detallado.

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más información.

