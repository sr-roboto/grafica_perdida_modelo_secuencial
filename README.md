# Predicción con TensorFlow.js

Este proyecto implementa un modelo de regresión lineal simple utilizando
TensorFlow.js. La aplicación permite:

- Entrenar un modelo de regresión en el navegador
- Visualizar la pérdida (loss) durante el entrenamiento
- Predecir múltiples valores simultáneamente

## Características

- **Entrenamiento del modelo**: Entrena un modelo de regresión utilizando
  TensorFlow.js directamente en el navegador.
- **Visualización de pérdida**: Gráfica interactiva que muestra cómo el error
  disminuye durante el entrenamiento.
- **Predicción múltiple**: Permite ingresar varios valores separados por comas
  para obtener predicciones simultáneas.
- **Interfaz sencilla**: Diseño limpio y fácil de usar.

## Requisitos

No se requiere instalación de dependencias extras ya que todas las bibliotecas
se cargan desde CDNs:

- TensorFlow.js
- Plotly.js

## Cómo ejecutar

Existen varias formas de ejecutar esta aplicación:

### Opción 1: Utilizando Live Server en Visual Studio Code

1. Instala la extensión "Live Server" en Visual Studio Code
2. Abre el archivo `index.html` en VS Code
3. Haz clic derecho sobre el archivo y selecciona "Open with Live Server"
4. La aplicación se abrirá automáticamente en tu navegador predeterminado

### Opción 2: Utilizando Python

Si tienes Python instalado:

```bash
# Python 3
python -m http.server

# Python 2
python -m SimpleHTTPServer
```

Luego abre tu navegador y ve a `http://localhost:8000`

### Opción 3: Utilizando Node.js

Si tienes Node.js instalado, puedes usar paquetes como `http-server`:

```bash
# Instalar http-server globalmente (solo la primera vez)
npm install -g http-server

# Ejecutar el servidor
http-server
```

Luego accede a `http://localhost:8080`

## Uso de la aplicación

1. Abre la aplicación en tu navegador
2. Haz clic en el botón "Entrenar Modelo" para entrenar la red neuronal
3. Observa cómo disminuye la pérdida en la gráfica durante el entrenamiento
4. Ingresa los valores para predecir en el campo de texto (separados por comas)
5. Haz clic en el botón "Predecir" para obtener los resultados

## Estructura del proyecto

```
├── index.html     # Archivo principal que contiene todo el código HTML, CSS y JavaScript
└── README.md      # Este archivo de documentación
```

## Cómo funciona

- El modelo se entrena con un conjunto de datos que sigue un patrón cuadrático
- Se utiliza un modelo de red neuronal con capas ocultas para capturar
  relaciones no lineales
- La visualización de la pérdida se actualiza durante el entrenamiento para
  mostrar el progreso
- Las predicciones se realizan utilizando el modelo entrenado en el navegador
  sin necesidad de un servidor

## Personalización

Puedes modificar los siguientes aspectos del código:

- **Datos de entrenamiento**: Cambia los arrays `xValues` e `yValues` para
  entrenar con tus propios datos
- **Arquitectura del modelo**: Modifica las capas y neuronas en la sección donde
  se crea el modelo
- **Hiperparámetros**: Ajusta el optimizador, tasa de aprendizaje, número de
  épocas, etc.
- **Visualización**: Personaliza la apariencia de las gráficas modificando las
  opciones de Plotly

## Limitaciones

- El modelo se ejecuta completamente en el navegador, lo que puede limitar el
  tamaño del conjunto de datos
- No hay persistencia del modelo (se pierde al recargar la página)
- La aplicación no guarda el historial de predicciones

## Autor

- Marcos Lopez
