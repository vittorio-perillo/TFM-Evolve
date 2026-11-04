# Entrega 00 — Equipos, ideas de producto y repositorio

**Máster:** Data Science e Inteligencia Artificial
**Centro:** Evolve
**Curso:** 2026–2027

**Repositorio:** [https://github.com/vittorio-perillo/TFM-Evolve](https://github.com/vittorio-perillo/TFM-Evolve)

---

## 2. Propuesta 1 — Optimizador inteligente del consumo eléctrico

### Título y descripción

**LuzSmart — Sistema inteligente de ahorro energético doméstico**

Desarrollar una plataforma basada en Data Science que permita a los hogares españoles optimizar su consumo eléctrico y reducir el importe de sus facturas.

El sistema analizará precios horarios, patrones de consumo y, cuando sea viable, predicciones del precio de la electricidad a corto plazo para generar recomendaciones personalizadas.

### Problema y usuario

El precio de la electricidad en la tarifa regulada PVPC varía a lo largo del día, lo que dificulta a los consumidores determinar cuándo resulta más económico utilizar determinados electrodomésticos.

Aunque existen aplicaciones que muestran los precios horarios, muchas ofrecen información general sin tener en cuenta los hábitos de consumo particulares de cada vivienda.

**Usuarios objetivo:** hogares españoles acogidos a la tarifa regulada PVPC que desean controlar y reducir sus gastos eléctricos.

Actualmente, estos usuarios consultan precios en páginas web o aplicaciones, comparan manualmente horarios y revisan sus facturas para intentar reducir el consumo.

### Uso y valor

Un usuario carga un archivo con su consumo eléctrico horario o introduce un perfil estimado de consumo.

La aplicación analiza sus hábitos y los relaciona con los precios de la electricidad.

Por ejemplo, puede identificar que utilizar una lavadora a determinadas horas permitiría reducir su coste respecto a su horario habitual.

El sistema presentará:

- Distribución horaria del consumo y del gasto estimado.
- Identificación de las horas económicamente más favorables.
- Recomendaciones para desplazar consumos flexibles.
- Estimación del ahorro potencial.
- Previsiones de precios cuando existan datos suficientes.

**Valor aportado:** transformar datos técnicos sobre electricidad en decisiones comprensibles y económicamente útiles para el usuario.

### Datos necesarios y fuentes

**Datos de electricidad**

- Red Eléctrica / e·sios: [https://www.esios.ree.es/](https://www.esios.ree.es/)
- Red Eléctrica: [https://www.ree.es/](https://www.ree.es/)

Se estudiará la disponibilidad de precios horarios históricos y otros indicadores que puedan resultar relevantes.

**Datos de consumo doméstico**

- Archivos horarios facilitados voluntariamente por usuarios.
- Datos simulados para desarrollar y demostrar el prototipo.

**Estado del acceso:** fuentes candidatas identificadas. Está pendiente confirmar las condiciones de acceso, la granularidad, la disponibilidad histórica y las restricciones de reutilización.

**Privacidad:** los datos de consumo doméstico pueden revelar patrones de presencia y actividad dentro del hogar. Se priorizarán datos ficticios, anonimizados o facilitados voluntariamente.

### Primera versión — MVP

La primera versión incluirá:

1. Importación de precios eléctricos horarios.
2. Carga de un perfil de consumo doméstico.
3. Visualización del consumo y del coste estimado por franjas horarias.
4. Identificación de horarios alternativos para consumos flexibles.
5. Estimación del ahorro económico al cambiar determinados hábitos.

**Demostración funcional:** el usuario carga un perfil de consumo y observa gráficamente cómo cambia su gasto estimado cuando modifica el horario de ciertos electrodomésticos.

**Fuera del MVP:** comparación exhaustiva de comercializadoras, recomendaciones de potencia contratada y predicciones a 72 horas sin validación suficiente.

### Viabilidad y dudas

La propuesta es viable como proyecto de Data Science, ya que existen fuentes oficiales, como Red Eléctrica y e·sios, que publican información sobre el mercado eléctrico español. Sin embargo, debemos comprobar qué datos históricos podemos obtener, su granularidad y las condiciones de acceso.

**Principales dificultades:**

- **Disponibilidad de datos:** necesitamos precios eléctricos históricos y perfiles de consumo horario de hogares. Podemos comenzar con datos simulados si no disponemos de consumos reales.
- **Precisión de las predicciones:** el precio eléctrico está influido por múltiples factores, como la demanda, la generación renovable y las condiciones meteorológicas. Debemos comprobar si nuestros modelos mejoran las predicciones de referencia.
- **Personalización:** las recomendaciones dependerán de los hábitos de consumo y de qué electrodomésticos pueden utilizarse en otros horarios.
- **Cálculo del ahorro:** será necesario distinguir entre el precio horario de la energía y el importe final de la factura, que incluye otros conceptos.

**¿Cómo comprobaremos su viabilidad?**

Primero verificaremos el acceso a los datos históricos y construiremos un pequeño dataset. Después, desarrollaremos un prototipo que calcule el coste del consumo de un hogar y simule cambios de horario.

Si conseguimos demostrar un ahorro potencial medible y razonable mediante estas simulaciones, tendremos una primera validación de la utilidad del producto.

La predicción de precios a 24–72 horas y la comparación de tarifas se plantearán como ampliaciones, dependiendo de la calidad y disponibilidad de los datos.

**Conclusión:** consideramos que la propuesta tiene una viabilidad técnica media-alta, especialmente si comenzamos con un simulador de consumo y ahorro antes de incorporar modelos predictivos avanzados.

---

## 3. Propuesta 2 — Predicción de saturación turística en España

### Título y descripción

**Tourism Insight — Plataforma predictiva de presión turística**

Desarrollar una plataforma de análisis de datos que permita estudiar la concentración turística en distintas regiones españolas e identificar destinos y épocas alternativas con menor presión.

Se pretende combinar estadísticas turísticas, modelos predictivos y visualizaciones geográficas para facilitar decisiones informadas.

### Problema y usuario

España recibe grandes cantidades de turistas que se concentran en determinadas ciudades, regiones y épocas del año.

Esta concentración puede provocar congestión, presión sobre los servicios públicos, impactos ambientales y dificultades para gestionar los recursos disponibles.

**Usuarios objetivo:**

- Viajeros que buscan destinos menos concurridos.
- Organismos de gestión turística.
- Administraciones públicas y profesionales de planificación turística.

Actualmente, estos usuarios recurren a estadísticas, informes, búsquedas en internet y comparaciones manuales para conocer la afluencia de visitantes.

### Uso y valor

Un usuario selecciona una región española y un periodo del año.

La plataforma muestra indicadores históricos de concentración turística, identifica patrones estacionales y, si los datos permiten entrenar un modelo fiable, presenta previsiones de afluencia.

Por ejemplo, una persona interesada en visitar las Islas Canarias podría comparar distintos meses o territorios para identificar periodos con menor actividad turística.

El sistema ofrecerá:

- Indicadores de concentración turística.
- Comparación entre regiones o periodos.
- Mapas interactivos.
- Visualización de tendencias.
- Posibles alternativas a destinos especialmente concurridos.

**Valor aportado:** facilitar decisiones de viaje y planificación turística mediante información cuantitativa, accesible y visual.

### Datos necesarios y fuentes

**Fuentes candidatas:**

- Instituto Nacional de Estadística (INE): [https://www.ine.es/](https://www.ine.es/)
- Portal de datos abiertos de España: [https://datos.gob.es/](https://datos.gob.es/)
- Eurostat: [https://ec.europa.eu/eurostat](https://ec.europa.eu/eurostat)

**Datos de interés:**

- Número de viajeros.
- Pernoctaciones.
- Ocupación de alojamientos.
- Distribución geográfica del turismo.
- Evolución mensual y estacional.
- Indicadores territoriales relevantes.

**Estado del acceso:** fuentes oficiales identificadas; está pendiente confirmar qué conjuntos ofrecen la resolución temporal y geográfica necesaria.

**Restricciones:** será necesario respetar las licencias de reutilización y evitar interpretar el número de visitantes como una medida directa y definitiva de saturación.

### Primera versión — MVP

La versión mínima incluirá:

1. Recopilación y limpieza de datos turísticos históricos.
2. Selección de un conjunto limitado de regiones españolas.
3. Análisis de tendencias y estacionalidad.
4. Construcción de indicadores comparables de actividad turística.
5. Desarrollo de un dashboard con gráficos y mapas interactivos.
6. Comparación de destinos y periodos alternativos.

**Demostración funcional:** el usuario selecciona una región y un mes; el dashboard muestra indicadores históricos, permite compararlos y presenta alternativas con menor concentración relativa.

**Fuera del MVP:** predicción de saturación a nivel de calle, monitorización en tiempo real y análisis exhaustivo de todos los municipios españoles.

### Viabilidad y dudas

La propuesta presenta una viabilidad inicial favorable porque España dispone de estadísticas oficiales de turismo publicadas por organismos como el Instituto Nacional de Estadística (INE) y diferentes portales de datos abiertos.

Nuestro objetivo será analizar **la totalidad del territorio español**, comparando comunidades autónomas y, cuando la disponibilidad de los datos lo permita, provincias y municipios.

**Principales dificultades:**

- **Disponibilidad y granularidad:** necesitamos comprobar qué indicadores turísticos están disponibles a escala nacional, autonómica, provincial y municipal, y con qué frecuencia se actualizan.
- **Definición de saturación turística:** un número elevado de visitantes no implica necesariamente saturación. Tendremos que definir indicadores que relacionen la actividad turística con las características del territorio, como plazas de alojamiento, población residente u ocupación.
- **Predicción:** la demanda turística depende de la estacionalidad, los festivos, los acontecimientos y otros factores externos. Será necesario comprobar si las series históricas permiten entrenar modelos predictivos suficientemente fiables.
- **Comparabilidad:** los datos de diferentes territorios pueden presentar diferencias metodológicas o periodos de cobertura distintos.
- **Recomendaciones:** los destinos alternativos deberán seleccionarse mediante criterios objetivos y no únicamente por presentar menos visitantes.

**¿Cómo comprobaremos su viabilidad?**

En primer lugar, verificaremos la disponibilidad de series históricas comparables para las comunidades autónomas españolas.

A continuación, desarrollaremos un análisis exploratorio para identificar patrones de estacionalidad y concentración turística. Utilizaremos modelos predictivos sencillos como referencia y evaluaremos posteriormente otros algoritmos, como XGBoost, si los datos lo justifican.

Por último, construiremos un prototipo de dashboard con un mapa de España que permita comparar territorios, periodos e indicadores turísticos.

La cobertura nacional será el objetivo del producto, aunque inicialmente podremos trabajar con datos agregados por comunidades autónomas para mantener un alcance viable.

**Conclusión:** consideramos que la propuesta tiene una viabilidad técnica media-alta. La principal incertidumbre es encontrar indicadores suficientemente representativos para medir la presión turística y generar recomendaciones fiables.

---

## 4. Propuesta 3 — Predicción del rendimiento de vídeos de cocina

### Título y descripción

**RecipePredict AI — Plataforma inteligente de análisis y optimización de contenido gastronómico**

Desarrollar una plataforma de Data Science e Inteligencia Artificial que ayude a creadores de contenido de cocina a analizar sus vídeos antes de publicarlos y estimar su rendimiento potencial.

La aplicación combinará información histórica del creador con características del contenido para identificar factores asociados a un mejor rendimiento y ofrecer recomendaciones personalizadas.

### Problema y usuario

Los creadores de contenido gastronómico publican vídeos en plataformas como TikTok, YouTube e Instagram sin disponer de una estimación personalizada sobre su rendimiento.

Aunque las plataformas proporcionan estadísticas de visualizaciones, interacciones y retención, normalmente estas métricas se conocen después de publicar. Además, interpretar qué características influyen en los resultados requiere comparar numerosos vídeos.

Las estrategias utilizadas por creadores con grandes audiencias no necesariamente funcionan en cuentas pequeñas, ya que cada canal tiene una audiencia, un estilo y un historial diferentes.

**Usuarios objetivo:** creadores de recetas y contenido gastronómico que quieran mejorar el rendimiento de sus publicaciones mediante el análisis de datos.

Actualmente, estos usuarios suelen consultar las estadísticas de cada plataforma, comparar manualmente publicaciones y probar distintos formatos mediante ensayo y error.

### Uso y valor

Un creador prepara un vídeo de una receta y, antes de publicarlo, lo sube a la aplicación junto con el título, la descripción y los hashtags previstos.

La plataforma analiza características del contenido, como la duración, el tipo de receta, la presencia de voz, el texto y determinados elementos visuales.

Posteriormente, compara estas características con el historial del propio creador y presenta:

- Una estimación de rendimiento bajo, medio o alto respecto a sus publicaciones anteriores.
- Los factores que el modelo considera más relevantes para la predicción.
- Comparaciones con vídeos anteriores de características similares.
- Entre tres y cinco recomendaciones de mejora basadas en patrones detectados.

Por ejemplo, la herramienta podría identificar que los vídeos de recetas de entre 30 y 45 segundos han obtenido históricamente mejores resultados en ese canal y sugerir ajustes en la duración de una nueva publicación.

Las recomendaciones se presentarían como hipótesis basadas en datos, no como garantías de conseguir más visualizaciones.

**Valor aportado:** ayudar a los creadores a tomar decisiones sobre sus publicaciones utilizando evidencias de su propio contenido, en lugar de depender únicamente de tendencias generales.

### Datos necesarios y fuentes

**1. Historial de contenido del creador**

Se dispone de una fuente candidata especialmente relevante: un canal propio de recetas con más de 100 vídeos publicados entre TikTok, YouTube e Instagram, incluyendo publicaciones que han alcanzado hasta 321.000 visualizaciones.

Datos de interés:

- Identificador y plataforma del vídeo.
- Fecha y hora de publicación.
- Duración.
- Título y descripción.
- Hashtags utilizados.
- Visualizaciones.
- Me gusta, comentarios y otras interacciones disponibles.
- Métricas de retención, cuando puedan obtenerse.
- Archivo audiovisual original, si está disponible.

**Estado del acceso:** la existencia del historial del canal ha sido comunicada por un integrante del equipo. Está pendiente verificar qué métricas pueden exportarse y si se dispone de los archivos originales.

**2. APIs oficiales**

Fuentes candidatas:

- YouTube Data API: https://developers.google.com/youtube/v3
- YouTube Analytics API: https://developers.google.com/youtube/analytics
- TikTok for Developers: https://developers.tiktok.com/
- TikTok Research API, únicamente si se cumplen sus requisitos de elegibilidad.
- Instagram Graph API, según los permisos y condiciones aplicables a la cuenta.

**Estado del acceso:** pendiente de verificar la autorización, los permisos específicos, las cuotas y las condiciones de utilización de cada API.

Se priorizarán exportaciones autorizadas del propio creador para evitar que el MVP dependa del acceso a todas las plataformas.

**3. Características extraídas del contenido**

Mediante herramientas de procesamiento de vídeo, audio y lenguaje natural se podrían obtener variables como:

- Duración del vídeo.
- Presencia de voz o música.
- Transcripción del contenido hablado.
- Palabras utilizadas en el título.
- Cantidad y tipo de hashtags.
- Categoría de receta.
- Características visuales de los primeros segundos.

**Privacidad y restricciones:** los vídeos y las métricas privadas se utilizarán con autorización de sus titulares. Se respetarán los términos de las plataformas y no se publicarán tokens, credenciales ni datos privados de audiencia.

### Primera versión — MVP

Para mantener un alcance viable, el primer prototipo se centrará en analizar el historial de un creador y elaborar recomendaciones mediante un modelo sencillo.

**Funciones mínimas:**

1. Importación de un dataset con las publicaciones históricas y sus métricas.
2. Limpieza y almacenamiento de información en una base de datos SQL.
3. Análisis exploratorio del rendimiento según duración, hashtags, tipo de receta y otras variables disponibles.
4. Cálculo de indicadores de rendimiento relativos al historial del creador, diferenciando plataformas cuando corresponda.
5. Desarrollo y evaluación de un modelo predictivo inicial que clasifique publicaciones por rendimiento, siempre que el volumen y la calidad de los datos lo permitan.
6. Dashboard en Streamlit con gráficos comparativos y recomendaciones basadas en patrones históricos.

**Demostración funcional:**

El usuario introduce las características de una publicación que todavía no ha realizado y recibe una estimación de rendimiento, si el modelo ha superado las pruebas de validación, junto con comparaciones históricas y recomendaciones.

**Fuera del MVP:**

- Análisis audiovisual automatizado completo mediante OpenCV y Whisper.
- Predicción universal para cualquier creador.
- Integración automática con las tres plataformas.
- Generación o edición automática de vídeos.
- Predicciones exactas del número de visualizaciones.

Estas funciones podrían incorporarse en fases posteriores.

### Viabilidad y dudas

La principal dificultad es disponer de suficientes datos históricos y determinar qué variables permiten predecir resultados de forma fiable.

Con aproximadamente 100 vídeos repartidos entre distintas plataformas, existe riesgo de sobreajuste y de obtener predicciones poco generalizables.

También será necesario considerar que las visualizaciones dependen de factores externos, como el tamaño de la audiencia, los algoritmos de recomendación y la antigüedad de cada publicación.

Para comprobar la viabilidad se propone:

- Verificar qué datos históricos están realmente disponibles.
- Analizar cuántas publicaciones comparables existen por plataforma.
- Definir un indicador de rendimiento normalizado respecto al creador.
- Evaluar modelos sencillos antes de utilizar algoritmos más complejos como XGBoost.
- Separar cronológicamente los datos de entrenamiento y evaluación.
- Utilizar únicamente variables conocidas antes de publicar para realizar las predicciones.
- Comparar los resultados del modelo con una predicción de referencia basada en el historial.

Como ampliación, se podrá estudiar el uso de SHAP para interpretar las predicciones y herramientas como OpenCV y Whisper para extraer características adicionales.

### Validación del producto

Se propone validar el sistema utilizando el canal de recetas del integrante del equipo.

Primero se analizará el historial existente para comprobar la capacidad predictiva del modelo con publicaciones anteriores no utilizadas en el entrenamiento.

Posteriormente, se podrán realizar pruebas con vídeos nuevos, registrando las recomendaciones aplicadas y su rendimiento real.

Esta evaluación permitirá comprobar si las recomendaciones resultan útiles. Para atribuir mejoras al producto será necesario controlar otros factores y, cuando sea posible, comparar publicaciones equivalentes.

**Resultado esperado:** una aplicación web desarrollada con Streamlit que permita analizar el historial de un creador de cocina, estudiar sus patrones de rendimiento y obtener recomendaciones personalizadas para futuras publicaciones.
|   |
| - |
|   |

