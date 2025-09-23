# Proyecto de Inteligencia Artificial: Predictor en Actividades Bancarias

**Fecha de entrega:** 30 de septiembre de 2025  
**Asignatura:** Técnicas en Inteligencia Artificial  
**Estudiante:** Omar Alberto Torres  
**Docentes:** Raúl Ramos Pollán, Jonathan Granda  
**Universidad:** Universidad de Antioquia  

## Descripción del Proyecto
Este proyecto implementa un modelo de **Machine Learning supervisado** para predecir si un cliente bancario aceptará una oferta de **depósito a plazo** tras una campaña de marketing.  

El objetivo es apoyar la toma de decisiones en estrategias comerciales, priorizando clientes con mayor probabilidad de conversión y reduciendo costos de campañas ineficientes.

## Fuente de Datos
- **Dataset:** Binary Classification with a Bank Dataset  
- **Plataforma:** Kaggle  
- **Competencia:** Tabular Playground Series - Season 5, Episode 8  
- **Enlace:** [Kaggle - Playground Series S5E8](https://www.kaggle.com/competitions/playground-series-s5e8/overview)  

El dataset incluye variables demográficas y económicas de clientes, y la variable `y` que indica aceptación (`1`) o rechazo (`0`) del producto.

## Requisitos del Sistema

### Hardware mínimo sugerido
- Procesador de 64 bits  
- 8 GB de RAM  
- 2 GB de espacio libre en disco  

### Software
- Python 3.11.4  
- Entorno recomendado: **Google Colab** (no requiere instalación adicional)  

### Librerías utilizadas
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- joblib  
- Otras

Estas librerías ya vienen instaladas por defecto en Google Colab.
Si deseas ejecutar el proyecto en tu equipo local, instálalas con el siguiente comando:

```bash
pip install pandas numpy scikit-learn matplotlib joblib
```
# funcionamiento del codigo
1. El notebook realiza los siguientes pasos:
2. Instalación y carga de librerías
3. Carga de automaticas de train.csv y test.csv desde Kaggle (Debes adquirir un json con el toque registrandose a la competencia).
4. Exploración preliminar de los datos.
5. Limpieza y codificación de variables categóricas.
6. Entrenamiento de un modelo de clasificación con Random Forest.
7. Evaluación con métricas: Accuracy, ROC-AUC y PR-AUC.
8. Exportación del modelo entrenado (modelo_entrenado.pkl).
9. Generación del archivo submission.csv con predicciones sobre el conjunto de prueba.
10. generación de modelo entrenado (mpdelo_entrenado.pkl)
9. Limitaciones actuales
10. No incluye validación cruzada ni optimización de hiperparámetros.
11. No incorpora técnicas avanzadas de ingeniería de características.
12. No está dockerizado ni expuesto como servicio web (fase futura).

# Cómo Ejecutar el Proyecto
1) Clone el repositorio

# Clonar el repositorio
```bash  
git clone https://github.com/hombremono873/proyecto_IA_Fase1_Fase_2_Fase3.git

```

# Abrir y ejecutar en Google Colab
**Nota**: Debes ingresar a la competencia cuyo link agrego nuevamente, e inscribirse en la competencia , obtener el json con token de acceso.
```bash  
   https://www.kaggle.com/competitions/playground-series-s5e8/overview

   ** Enlace directo a datos **
   https://www.kaggle.com/competitions/playground-series-s5e8/data
 ```
1. Subir modelo_predictor_banco.ipynb a Colab.
2. Ejecute el rung de instalación de librerías run [1]
3. Instale la librería de kaggle en el run[2]
4. Seleccione tu archivo kaggle.json en el run[3]
5. Carga del json en el ambiente de colab en el run[4]
6. Ejecute la descarga de los archivos train.csv y test.csv al ambiente de cola en el run[5]
7. Desspues de descargados los datasets proceda a ejecutar los run que siguen en orden consecutivo.
8. Finalizado el proceso se vera las predicciones realizadas con el repositorio test.csv,
   El codigo genera un archivo con las predicciones sample_submission.csv y el modelo entrenado (modelo_entrenado.pkl) 
   en la carpeta de descargas.
   Tambien se vera en el ambiente de colab como salida el Val Accuracy, Val ROC_AUC, VAl_PR-AUC y Calassification Report.
   Tenga en cuenta que el modelo es desbalanceado en los ceros (Se entrenó con un dataset donde los ceros son el valor mayoritario).
**Nota Final**
En la documentación hecha en el mismo archivo de colab tambien encontrará las direcciones a la competencia de donde se estrajo los datos
para realizar este trabajo   
```

# Contacto
Para dudas o contribuciones:
Omar Alberto Torres
Correo: omara.torres@udea.edu.co
Cel: 3043440112