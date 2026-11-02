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

---

## 4. Propuesta 3 — Pendiente de definir

**Título:** pendiente.

**Descripción:** pendiente.

**Problema y usuario:** pendiente.

**Uso y valor:** pendiente.

**Datos y fuentes candidatas:** pendiente.

**Primera versión (MVP):** pendiente.

**Viabilidad y dudas:** pendiente.

|   |
| - |
|   |

