# Predicción de precios de vivienda (TC4058, Equipo 19)

Actividad 6 del curso *Inteligencia artificial y aprendizaje automático*, de la Maestría en Inteligencia Artificial Aplicada del Tecnológico de Monterrey.

Integrantes: Jorge Hernández Montero (A01733616), Carla Estefanía Hidalgo Horta (A01018380), Carlos Manuel Hernández Gutiérrez (A00812506) y Karla Berenice Hernández Centeno (A01797382).

El cuaderno `PreciosVivienda_Equipo19.ipynb` compara regresión lineal (OLS, Ridge, Lasso y Elastic-Net), árbol de decisión, bosque aleatorio, XGBoost, MLP y SVR, además de VotingRegressor y StackingRegressor, para predecir `SalePrice`. El cuaderno se sube ya ejecutado, así que GitHub muestra todas las salidas sin correrlo.

| Archivo | Contenido |
| --- | --- |
| `PreciosVivienda_Equipo19.ipynb` | Cuaderno ejecutado, con código, salidas y reportes |
| `requirements.txt` | Versiones exactas de las bibliotecas con las que se ejecutó |
| `.gitignore` | Excluye los datos de Kaggle |

## Datos

Los datos no se incluyen en el repositorio porque las reglas de Kaggle restringen su redistribución. Descarga `train.csv` del reto [House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data) (requiere una cuenta de Kaggle y aceptar las reglas del reto) y colócalo junto al cuaderno. Con la CLI de Kaggle: `kaggle competitions download -c house-prices-advanced-regression-techniques`, y después descomprime el zip.

Archivo esperado: `train.csv` de 1,460 filas y 81 columnas, SHA-256 `1e18addf81e5e4d347cc17ee6075bbe4a42b7fa26b9e5b063e8f692a5f929d41`. Para verificarlo: `sha256sum train.csv` (Linux), `shasum -a 256 train.csv` (macOS) o `Get-FileHash train.csv` (PowerShell).

## Cómo reproducirlo

Requiere Python 3.12 o posterior (se ejecutó con Python 3.13.17).

```bash
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter execute --inplace PreciosVivienda_Equipo19.ipynb
```

También puede abrirse en Jupyter o VS Code y ejecutar todas las celdas en orden. En Google Colab, sube `train.csv` y `requirements.txt`, ejecuta `!pip install -r requirements.txt`, reinicia la sesión y después corre el cuaderno.

La ejecución completa tarda unos 15 minutos con 2 núcleos. Con estas versiones y el mismo `train.csv` las métricas se reproducen; en otro procesador pueden variar en las últimas cifras, y los tiempos medidos cambian.
