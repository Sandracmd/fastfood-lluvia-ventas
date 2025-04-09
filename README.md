# fastfood-lluvia-ventas
Este proyecto analiza cómo influye la cantidad de lluvia en el volumen de ventas por hora en distintas regiones.

OBJETIVO
Determinar si existe una relación estadísticamente significativa entre la variable climática lluvia_promedio y las ventas_por_hora.

TECNOLOGÍAS UTILIZADAS
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Random Forest
MySQL y MongoDB

¿QUÉ SE HIZO?
- Se conectaron las bases de datos MySQL (ventas) y MongoDB (clima). En MySQL se obtienen las tablas `ventas`, `ticket` y `tiendas`. En MongoDB se accede a las colecciones `Ubicacion_sensores` y `sensor_eventos`.

- PROCESO ETL
  - Se unifican los datos de ventas con tickets y tiendas.
  - Se agregan datos climáticos de lluvia por región y hora, redondeando la fecha.
  - Se agrupa el total de ventas por hora y región para análisis.

- MODELADO PREDICTIVO
  - Se entrenaron tres modelos distintos para evaluar la relación entre la lluvia y las ventas:
    - Regresión lineal
    - Regresión polinomial
    - Random Forest Regressor  

RESULTADOS
- La regresión lineal obtuvo un R² de aproximadamente 0.0002, indicando que no existe una relación lineal significativa.

- Los modelos polinomial y de bosque aleatorio también mostraron baja capacidad predictiva, lo que sugiere que la lluvia no influye fuertemente en las ventas en este contexto.

CÓMO CORRER EL PROYECTO
- Abrir el archivo .ipynb en Google Colab o Jupyter.
  
- Configurar credenciales de acceso a MySQL y MongoDB.

- Ejecutar todas las celdas paso a paso.

CONCLUSIONES
- No se encontró una correlación clara entre las ventas por hora y el nivel de lluvia.

- Puede ser útil agregar más variables (como temperatura, día de la semana o promociones) para mejorar los modelos predictivos.
