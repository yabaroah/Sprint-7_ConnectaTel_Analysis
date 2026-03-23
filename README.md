# Sprint-7_ConnectaTel_Analysis
El objetivo del proyecto es identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.
Proyecto 6 - Análisis de una empresa de telecomunicaciones

Introducción
ConnectaTel es una empresa de telecomunicaciones con operaciones en México y Colombia que requiere identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.
Se cuenta con tres fuentes de datos:
•	plans.csv: los planes actuales 
•	users.csv: información de clientes
•	usage.csv: el detalle de uso real
Se debe explorar, limpiar y analizar estas bases de datos para construir una visión clara, confiable y accionable sobre el comportamiento de uso de los clientes y cómo varía entre diferentes grupos de usuarios.
________________________________________
💡 Objetivos:
•	Segmentación de clientes para mostrar mayor o menor uso de llamadas y mensajes.
•	Detección y diagnóstico de valores atípicos que puedan indicar comportamientos inusuales, fraude o errores de registro.
•	Análisis de la variación del uso según la edad y el tipo de plan contratado.
•	Identificación de patrones que ayuden a diseñar mejores planes, optimizar la oferta y mejorar la satisfacción del cliente.

📝 Plan de acción (pensamiento programático)

1.	Integrar y limpiar bases de datos provenientes de tres fuentes distintas.
2.	Aplicar técnicas de validación, estandarización de tipos de datos y detección de valores inconsistentes.
3.	Construir un perfil estadístico del uso (llamadas y mensajes) por cliente y por segmentos demográficos.
4.	Detectar outliers y comportamientos atípicos mediante métodos estadísticos y visuales.
5.	Crear segmentaciones de clientes basadas en edad, país y comportamiento de uso.
6.	Visualizar diferencias entre segmentos y extraer insights comerciales relevantes.
   
Datasets del Proyecto
Se trabaja con tres fuentes principales de información, relacionadas con usuarios, actividad y planes del servicio de telecomunicaciones:

1.	plans.csv: Catálogo de planes con sus precios y beneficios. 
  2 registros, 8 columnas 
plan_name            Nombre del plan       
messages_included    Mensajes incluidos en el plan  
gb_per_month         GB incluidos por mes       
minutes_included     Minutos de llamada incluidos en el plan por mes   
usd_monthly_pay      Pago mensual    
usd_per_gb           Pago por GB adicional         
usd_per_message      Pago por mensaje adicional    
usd_per_minute       Pago por minute adicional  
   
2.	users_latam.csv: Información de cada usuario 
  4000 registros, 8 columnas
user_idIdentificador de usuario
first_name  			Nombre del usuario
 last_name   			Apellido del usuario
 age				Edad del usuario 
 city        			Ciudad 
 reg_date   	 		Fecha de registro
 plan        			Tipo de plan
 churn_date			Fecha de abandono

4.	usage.csv: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud.  
  40000  registros, 6 columnas 
id        			Identificador del servicio
user_id   		Identificador del usuario
type 			Tipo de servicio (llamada/mensaje)    
date      		Fecha del servicio
duration  		Duración de llamada (minutos)
length  		Longitud del mensaje (caracteres)
  
Contexto del negocio
Analizar el negocio usando los 3 datasets para que ConnectaTel entienda cómo se comportan sus usuarios según edad, volumen de llamadas/mensajes y nivel de consumo. El entregable será un análisis completo (distribuciones, outliers, segmentación y oportunidades comerciales) acompañado de un notebook limpio y reproducible.

🔄 Flujo general del proyecto
Paso	Acción	Resultado para el negocio
1. Cargar y explorar	Cargar y explorar plans, users_latam, usage.
	Visión clara de la estructura y tipos de columna de cada dataset.
2. Identificación de problemas de calidad	Contar nulos, detectar sentinels, revisar fechas fuera de rango.	Lista priorizada de problemas que pueden sesgar decisiones.
3. Limpieza básica	Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas.	Datos consistentes y listos para análisis estadístico.
4. Summary statistics	Revisar las medidas clave en variables categóricas y numéricas.	Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo
5. Visualización & outliers	Creación de histogramas y boxplots.	Visualización de sesgos, patrones de usuarios o datos atípicos.
6. Segmentación	Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots.	Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.
7. Insight ejecutivo	Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores.	Responder a las preguntas del negocio y proponer acciones concretas.
		
▶ Cómo abrir el notebook en Google Colab
1.	Abre el archivo .ipynb en GitHub
2.	Haz clic en Open in Colab
