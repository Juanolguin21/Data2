ANTE CUALQUIER INCONVENIENTE CON LA APERTURA DEL COLAB; CONCULTAR EL DRIVE

https://colab.research.google.com/drive/1mW0Fbf15E30vq_OBrkifOWQdkKyl6sKh#scrollTo=ujlzGcDv1tcD

Somos detectives financieros, encargados de comprender la dinámica de una institución crediticia en Argentina. Nuestro objetivo principal es obtener información sobre el comportamiento del cliente, el uso de tarjetas de crédito y el rendimiento de los préstamos. Al explorar las relaciones dentro de los datos, buscamos identificar oportunidades para el crecimiento, la mitigación de riesgos y la mejora del servicio al cliente.

Personajes :

Clientes: Esta hoja presenta a nuestro elenco. Contiene información demográfica, ubicación (Zonal, Sucursal) y datos de contacto. Estos son los individuos cuyas vidas financieras estamos a punto de explorar.

TC (Tarjetas de Crédito): Esta hoja detalla la actividad de las tarjetas de crédito de nuestros clientes. Revela hábitos de gasto, límites de crédito y comportamientos de pago.

Préstamos: Esta hoja describe la cartera de préstamos. Contiene información sobre tipos de préstamos, montos, tasas de interés y calendarios de pago.
Trama (Análisis Exploratorio):

Acto 1: Conociendo a los Clientes 

La Escena Inicial: Comenzamos perfilando nuestra base de clientes.

¿Cuántos clientes hay en el conjunto de datos?
¿Cuál es la distribución de clientes en las diferentes regiones "Zonal"? ¿Qué regiones tienen la mayor concentración de clientes?
¿Cuántos clientes hay en cada "Sucursal" (oficina)? ¿Hay sucursales específicas con una base de clientes particularmente grande o pequeña?
Desarrollo de Personajes: Profundizamos en los perfiles individuales de los clientes.
¿Existen patrones discernibles en las direcciones de correo electrónico proporcionadas (por ejemplo, dominios comunes, correos personales frente a correos comerciales)?
¿Qué tan completa es la información de contacto? ¿Faltan direcciones de correo electrónico o números de teléfono que podrían dificultar la comunicación?
¿Qué podemos inferir del campo "Nombre completo"? ¿Hay apellidos o grupos étnicos comunes representados?

Acto 2: El Mundo del Crédito 

Acción Ascendente: Cambiamos nuestro enfoque al uso de tarjetas de crédito.
¿Cuáles son las métricas clave disponibles en la hoja TC (por ejemplo, montos de gasto, límites de crédito, fechas de pago)?
¿Cuál es el gasto promedio con tarjeta de crédito por cliente? ¿Cómo varía esto entre diferentes regiones u oficinas?
¿Cuál es la distribución de los límites de crédito? ¿Existen distintos niveles de solvencia entre nuestros clientes?
Conflictos y Desafíos: Examinamos los riesgos potenciales y las áreas de preocupación.
¿Cuál es la tasa de utilización de crédito promedio (gasto / límite de crédito)? ¿Hay clientes con tasas de utilización excesivamente altas, lo que indica una posible tensión financiera?
¿Hay pagos atrasados o pagos omitidos? ¿Cuál es la frecuencia y gravedad de estos problemas?

Acto 3: El Panorama de los Préstamos 

Clímax: Analizamos la cartera de préstamos y su rendimiento.
¿Qué tipos de préstamos son más comunes ("Campaña de Préstamos")?
¿Cuál es el monto promedio del préstamo y la tasa de interés? ¿Cómo varían estos entre los diferentes tipos de préstamos?
¿Cómo es el rendimiento de los préstamos? ¿Hay incumplimientos o morosidades?
Entrelazando las Historias: Comenzamos a conectar las diferentes hojas de datos.
¿Los clientes con tarjetas de crédito también tienden a solicitar préstamos?
¿Existe una correlación entre los hábitos de gasto con tarjeta de crédito y el comportamiento de pago de los préstamos?
¿Hay datos demográficos o regiones de clientes específicos que son más propensos a los incumplimientos de préstamos?
Acto 4: Resolución e Ideas

La Imagen Completa: Sintetizamos nuestros hallazgos para sacar conclusiones significativas.
¿Cuáles son los principales impulsores del rendimiento de los préstamos?
¿Existen oportunidades sin explotar para la venta cruzada o el aumento de la venta de productos financieros?
¿Cómo puede la institución crediticia gestionar mejor el riesgo y mejorar las relaciones con los clientes?
La Moraleja de la Historia: Identificamos recomendaciones prácticas basadas en nuestro análisis.
Desarrollar campañas de marketing dirigidas a segmentos de clientes específicos.
Implementar estrategias de mitigación de riesgos para prestatarios de alto riesgo.
Mejorar el servicio al cliente para aumentar la satisfacción y la lealtad.
Epílogo (Exploración Adicional):

Esto es solo el comienzo. Podríamos enriquecer aún más nuestro análisis incorporando fuentes de datos externas, como indicadores económicos o información de la competencia.
Preguntas Clave para Guiar la Exploración:

¿Cuáles son las características de nuestros clientes más valiosos?
¿Cuáles son los mayores riesgos para nuestra cartera de préstamos?
¿Cómo podemos adaptar mejor nuestros productos y servicios para satisfacer las necesidades de nuestros clientes?

MACHINE LEARNING

Abstracto (Motivación y Audiencia)
Este cuaderno tiene como objetivo analizar un conjunto de datos que contiene información sobre individuos, incluyendo su CUIL, detalles de campañas de préstamos, ubicación geográfica, información de contacto y otros atributos relevantes. La motivación principal es aprovechar estos datos para predecir la probabilidad de éxito de las solicitudes de préstamo o identificar clientes potenciales para campañas de préstamos dirigidas. Este análisis puede beneficiar a las instituciones financieras, los equipos de marketing y los departamentos de evaluación de riesgos, permitiéndoles tomar decisiones basadas en datos relacionados con aprobaciones de préstamos, estrategias de marketing y segmentación de clientes.

Preguntas/Definición del problema
El principal problema que abordaremos es un problema de clasificación:

Objetivo: Predecir si es probable que un individuo sea un buen candidato para un préstamo o un objetivo receptivo para una campaña de préstamos. Variable objetivo: Necesitaremos diseñar una variable objetivo basada en los datos disponibles. Por ejemplo, esto podría ser una variable binaria que represente si el individuo tiene "Paquetes" (packages) o "Cartera abierta" (open portfolio); uno podría etiquetarse como "probable que esté interesado en un préstamo" y el otro como "menos probable".

Breve análisis exploratorio de datos (EDA)
Realizaré un EDA inicial, que incluirá:

Inspección de datos: Mostrar las primeras filas, verificar los tipos de datos e identificar posibles problemas. Estadísticas descriptivas: Calcular estadísticas resumidas (media, mediana, desviación estándar, etc.) para características numéricas para comprender sus distribuciones. Visualización de datos: Histogramas de características numéricas Gráficos de barras de características categóricas. Mapa de calor de correlación para identificar relaciones entre características numéricas. Análisis de valores faltantes: Identificar y cuantificar los valores faltantes en cada columna.

Ingeniería de características
Diseñaré nuevas características y transformaré las existentes, como:

Crear una variable objetivo: Definir una regla para crear una variable objetivo binaria. Características geográficas: Tal vez extraer la ciudad de 'Sucursal' o crear zonal y sucursal combinadas. Características de correo electrónico: Crear una característica que indique el número de direcciones de correo electrónico disponibles (0, 1, 2 o 3). Número de teléfono: Limpiar los datos del número de teléfono y convertirlo en una variable binaria: disponible sí/no. Escalado de características numéricas: Estandarizar o normalizar características numéricas. Codificación de características categóricas: Codificar características categóricas (por ejemplo, 'Zonal', 'Sucursal') utilizando codificación one-hot u otros métodos apropiados.

Entrenamiento y prueba
Entrenaré y evaluaré al menos dos modelos diferentes de aprendizaje automático:

Modelos: Regresión logística: Modelo simple e interpretable para clasificación. Bosque aleatorio: Potente método de conjunto para la clasificación, capaz de capturar relaciones no lineales. Validación cruzada: Utilizar la validación cruzada k-fold para evaluar el rendimiento del modelo y evitar el sobreajuste.

Optimización
Optimizaré los hiperparámetros del modelo utilizando una técnica como GridSearchCV o RandomizedSearchCV para encontrar la mejor configuración del modelo.

Selección del modelo
Seleccionaré el mejor modelo basándome en métricas apropiadas para la clasificación:

Métricas: AUC (área bajo la curva ROC): para evaluar la capacidad del modelo para discriminar entre clases. Precisión, exhaustividad y puntuación F1: para una evaluación exhaustiva del rendimiento de la clasificación.


Conclusión:

El análisis buscó predecir la propensión a préstamos y segmentar clientes. Random Forest fue el mejor modelo, con hiperparámetros max_depth=10, n_estimators=200, y n_clusters=7, obteniendo un AUC de 0.5776 en el conjunto de prueba.

Hallazgos: Si bien el modelo puede discriminar relativamente bien entre clases (AUC 0.5776), tiene una precisión baja (0.1590), lo que indica muchos falsos positivos, y un recall de 0.5140. Esto implica que identifica correctamente solo la mitad de los potenciales interesados en un préstamo.

Recomendaciones:

Considerar otros modelos o técnicas de mejora para aumentar la precisión. Analizar las características de los clientes en cada clúster para diseñar estrategias de marketing y evaluación de riesgo personalizadas. Limitaciones:

Debido al AUC modesto, se recomienda usar este modelo con precaución y complementarlo con otras fuentes de información y criterio experto.
