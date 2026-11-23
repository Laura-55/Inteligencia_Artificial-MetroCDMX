# 🚇 Inteligencia Artificial-MetroCDMX

### Optimización de rutas del Metro de Ciudad de México mediante Inteligencia Artificial

Aplicación desarrollada en **Python** para el cálculo y la visualización de rutas óptimas del Metro de Ciudad de México (CDMX), utilizando el algoritmo de búsqueda informada **A\*** y la representación de la red de transporte mediante grafos.

El sistema permite encontrar el trayecto más eficiente entre dos estaciones, considerando los tiempos de desplazamiento, los transbordos, los horarios de funcionamiento y las condiciones de accesibilidad para personas con movilidad reducida.

## 🎯 Objetivos

- Modelar la red del Metro de Ciudad de México mediante un grafo ponderado.
- Implementar el algoritmo **A\*** para encontrar rutas óptimas.
- Minimizar el tiempo estimado de desplazamiento, incluyendo los transbordos.
- Incorporar restricciones de accesibilidad para personas con movilidad reducida.
- Considerar el día y la hora del trayecto en la estimación del tiempo.
- Desarrollar una interfaz gráfica intuitiva que permita visualizar las rutas calculadas.

## ⚙️ Funcionalidades

### 🔍 Cálculo de rutas óptimas

Búsqueda del trayecto de menor coste temporal entre dos estaciones mediante el algoritmo A\*, utilizando una matriz heurística de tiempos estimados.

### ♿ Accesibilidad

Opción para comprobar las condiciones de accesibilidad de las estaciones de origen, destino y transbordo para personas con movilidad reducida.

### 🕒 Estimación de tiempos

Cálculo del tiempo total estimado considerando:

- Tiempo de desplazamiento entre estaciones.
- Tiempo necesario para realizar transbordos.
- Día de la semana y horario de apertura del metro.
- Penalización temporal en fines de semana.

### 🗺️ Visualización interactiva

Interfaz gráfica que permite:

- Seleccionar las estaciones de origen y destino.
- Indicar el día y la hora del trayecto.
- Activar la opción de ruta accesible.
- Consultar el recorrido y los transbordos necesarios.
- Visualizar la ruta sobre el mapa del metro.
- Observar una animación del tren siguiendo el trayecto calculado.

## 🧠 Algoritmo A\*

El proyecto utiliza el algoritmo de búsqueda informada **A\***, que permite encontrar caminos de coste mínimo combinando el coste acumulado y una estimación del coste restante.

La función de evaluación utilizada es:

**f(n) = g(n) + h(n)**

Donde:

- **g(n):** coste acumulado desde la estación de origen hasta el nodo actual.
- **h(n):** estimación heurística del tiempo necesario para llegar desde el nodo actual hasta el destino.
- **f(n):** estimación del coste total del camino que pasa por el nodo actual.

La red se representa mediante un grafo ponderado, cuyos nodos identifican estaciones y líneas de metro, mientras que las aristas representan conexiones y transbordos con sus respectivos costes temporales.

El modelo implementado contempla **35 estaciones de 5 líneas** del Metro CDMX (1, 3, 7, 9 y 12), junto con sus correspondientes conexiones y transbordos.

## 🛠️ Tecnologías utilizadas

- **Python:** lenguaje principal de desarrollo.
- **NetworkX:** representación y gestión del grafo y aplicación del algoritmo A\*.
- **Tkinter:** desarrollo de la interfaz gráfica de escritorio.
- **Pillow (PIL):** procesamiento y visualización de imágenes.
- **Estructuras de datos y matrices heurísticas:** modelado de estaciones, conexiones, accesibilidad y tiempos estimados.

## 📁 Estructura del proyecto

```text
IA-MetroCDMX/
│
├── metro.py                 # Grafo, heurística y cálculo de rutas
├── metro_interfaz.py        # Interfaz gráfica y animación
├── MapaMetroCDMX.png        # Mapa del metro
├── tren.png                 # Imagen del tren
└── README.md                # Documentación del proyecto
```

## 🚀 Instalación y ejecución

**1. Clonar el repositorio**

```bash
git clone https://github.com/USUARIO/IA-MetroCDMX.git
cd IA-MetroCDMX
```

Sustituye `USUARIO` por el nombre del propietario del repositorio.

**2. Instalar las dependencias**

Es necesario disponer de Python 3 y de Tkinter en el entorno de ejecución.

```bash
pip install networkx pillow
```

**3. Ejecutar la aplicación**

```bash
python metro_interfaz.py
```

Se abrirá una ventana en la que podrás seleccionar las estaciones, configurar las condiciones del viaje y calcular la ruta.

## 📍 Ejemplo de utilización

1. Seleccionar **Universidad** como estación de origen.
2. Seleccionar **Polanco** como estación de destino.
3. Indicar el día de la semana y la hora.
4. Activar, si se desea, la opción de accesibilidad.
5. Pulsar **Calcular ruta**.

La aplicación mostrará el recorrido calculado, el tiempo estimado y los transbordos necesarios, representando visualmente la ruta en el mapa mediante una animación.

## 🎓 Contexto académico

Proyecto desarrollado en el marco de la asignatura de **Inteligencia Artificial** del Grado en Ingeniería Informática de la **Universidad Politécnica de Madrid (UPM)**.

Su desarrollo permitió aplicar conocimientos de búsqueda heurística, teoría de grafos, optimización de caminos y desarrollo de interfaces gráficas a un problema práctico de planificación de rutas de transporte público.

## 📝 Consideraciones

El proyecto utiliza una representación parcial de la red del Metro CDMX, limitada a las estaciones y líneas contempladas en la práctica académica.

Los tiempos utilizados son estimaciones del modelo y no representan información en tiempo real. La comprobación de accesibilidad se basa en los datos definidos en la aplicación y no constituye una garantía de accesibilidad actual de las instalaciones.

---

**Proyecto académico | Inteligencia Artificial | Universidad Politécnica de Madrid**
