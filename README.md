# Visualización de Celdas GRACE con Límite de Acuífero

Este script genera un mapa temático a partir de datos **GRACE**, mostrando la distribución de valores de **almacenamiento de agua subterránea (GWS)** para el primer día del registro.

## Características

- **Transformación de coordenadas** de latitud/longitud a proyección **Web Mercator** (EPSG:3857).
- **Superposición de cuadrícula enumerada** (36 celdas) sobre el área de estudio.
- **Resaltado del límite del acuífero** reproyectado.
- **Líneas de grilla** y etiquetas numéricas en el centro de cada celda.
- **Mapa base** de Esri con transparencia ajustada para visualizar datos y contexto geográfico.
- **Barra de color** representando valores GWS en milímetros.

## Flujo General del Script

1. **Carga de datos** desde CSV con coordenadas en grados.
2. **Definición de bordes y centros** de celdas GRACE.
3. **Transformación de coordenadas** de 4326 → 3857 para visualización.
4. **Dibujo del mapa**:
   - Capa de valores GWS.
   - Cuadrícula de celdas.
   - Etiquetas de numeración.
   - Límite del acuífero.
5. **Exportación** de la imagen final en alta resolución (`.png`).

## Requisitos

- Python 3.8+
- Librerías:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `geopandas`
  - `contextily`
  - `pyproj`

Instalación rápida de dependencias:

```bash
pip install numpy pandas matplotlib geopandas contextily pyproj
