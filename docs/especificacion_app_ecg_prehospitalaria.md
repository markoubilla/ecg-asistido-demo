# Especificacion inicial de app movil para lectura asistida de ECG

## 1. Nombre tentativo

ECG Prehospitalario Asistido

## 2. Proposito

Desarrollar una aplicacion movil de apoyo clinico para personal de atencion prehospitalaria, postas rurales, SAPU, SAR y servicios de urgencia, capaz de capturar imagenes de monitores cardiacos, tiras de ritmo o electrocardiogramas de 12 derivaciones, procesarlas y entregar una interpretacion orientativa de hallazgos criticos.

La aplicacion no reemplaza el criterio clinico ni establece diagnosticos definitivos. Su funcion principal es apoyar la priorizacion, la sospecha diagnostica y la comunicacion temprana con equipos intrahospitalarios.

## 3. Problema a resolver

En escenarios prehospitalarios y rurales, muchas decisiones deben tomarse con recursos limitados, conectividad irregular y acceso diferido a especialistas. La interpretacion de trazados cardiacos puede variar segun experiencia del operador, calidad del registro, tipo de monitor disponible y tiempo de traslado.

Una herramienta movil podria ayudar a:

- Estandarizar la lectura inicial de trazados.
- Alertar sobre hallazgos potencialmente criticos.
- Reducir retrasos en derivacion o activacion de redes de urgencia.
- Registrar evidencia visual del ECG o monitor.
- Comparar la sospecha inicial con diagnosticos confirmados posteriormente.

## 4. Usuarios objetivo

- Tecnicos en enfermeria de nivel superior en ambulancias, SAPU, SAR y postas.
- Enfermeros/as de urgencia o atencion rural.
- Medicos generales en servicios de urgencia de baja y mediana complejidad.
- Equipos SAMU o de traslado secundario.
- Coordinadores clinicos o medicos reguladores.

## 5. Alcance clinico inicial

La primera version debe enfocarse en hallazgos de alto impacto y lectura basica robusta, evitando prometer diagnosticos complejos desde el inicio.

### Hallazgos prioritarios del MVP

- Frecuencia cardiaca aproximada.
- Ritmo regular o irregular.
- QRS angosto o ancho.
- Bradicardia significativa.
- Taquicardia significativa.
- Sospecha de fibrilacion auricular.
- Sospecha de taquicardia de complejo ancho.
- Sospecha de bloqueo AV avanzado.
- Sospecha de supradesnivel del ST en ECG de 12 derivaciones.
- Calidad insuficiente de imagen o trazado no interpretable.

### Hallazgos para fases posteriores

- Localizacion probable de IAM con supradesnivel ST.
- Depresion del ST y cambios isquemicos sutiles.
- QT corregido.
- Hiperkalemia sugerida por patron electrocardiografico.
- Bloqueos de rama.
- Criterios de Sgarbossa modificados.
- Ritmos de marcapasos.
- Comparacion con ECG previos.

## 6. Flujo principal de uso

1. El usuario abre la app.
2. Selecciona el tipo de captura:
   - Monitor cardiaco.
   - Tira de ritmo.
   - ECG de 12 derivaciones.
3. La app muestra una guia visual para encuadrar la imagen.
4. El usuario toma la foto.
5. La app evalua calidad:
   - Nitidez.
   - Iluminacion.
   - Perspectiva.
   - Presencia de derivaciones o trazado visible.
6. Si la imagen es deficiente, solicita repetir captura.
7. Si es aceptable, procesa el trazado.
8. Entrega resultado orientativo con:
   - Hallazgos detectados.
   - Nivel de urgencia.
   - Confianza del analisis.
   - Recomendacion operativa.
9. El usuario puede guardar, compartir o enviar el caso a regulacion medica o centro receptor.
10. Posteriormente se registra el diagnostico confirmado intrahospitalario.

## 7. Niveles de resultado sugeridos

### Rojo: alerta critica

Posible condicion tiempo-dependiente o potencialmente inestable.

Ejemplos:

- Sospecha de IAM con supradesnivel ST.
- Taquicardia de complejo ancho.
- Bradicardia severa con signos de inestabilidad.
- Ritmo irregular rapido compatible con arritmia significativa.

Accion sugerida:

- Evaluar ABCDE y signos de inestabilidad.
- Obtener o repetir ECG de 12 derivaciones si es posible.
- Contactar regulacion medica o centro receptor.
- Considerar traslado prioritario segun protocolo local.

### Amarillo: requiere evaluacion clinica

Hallazgos no concluyentes o potencialmente relevantes.

Ejemplos:

- Alteraciones inespecificas del ST-T.
- Ritmo irregular sin criterio claro.
- QRS ancho sin taquicardia.
- ECG interpretable parcialmente.

Accion sugerida:

- Correlacionar con sintomas, signos vitales y antecedentes.
- Repetir ECG si hay dolor toracico, disnea, sincope o deterioro.
- Solicitar evaluacion medica.

### Verde: sin hallazgos criticos evidentes

No se detectan alteraciones criticas en la imagen analizada.

Accion sugerida:

- Mantener evaluacion clinica.
- No descartar patologia cardiaca solo por este resultado.
- Confirmar con examenes si el cuadro clinico lo justifica.

### Gris: no interpretable

La imagen o el trazado no permite una lectura confiable.

Accion sugerida:

- Repetir captura.
- Mejorar iluminacion.
- Evitar reflejos.
- Alinear ECG o monitor.
- Registrar ECG directo si hay equipo disponible.

## 8. Funcionalidades principales

### Captura guiada

- Marco para ECG de 12 derivaciones.
- Marco para monitor cardiaco.
- Indicador de enfoque y luz.
- Deteccion de bordes del papel o pantalla.
- Correccion automatica de perspectiva.

### Procesamiento de imagen

- Recorte automatico.
- Correccion de inclinacion.
- Aumento de contraste.
- Reduccion de ruido.
- Identificacion de cuadricula si existe.
- Separacion de derivaciones en ECG impreso.

### Extraccion de senal

- Deteccion del trazo electrocardiografico.
- Conversion aproximada de pixeles a tiempo y amplitud.
- Reconocimiento de complejos QRS.
- Estimacion de intervalos cuando sea posible.

### Analisis clinico asistido

- Medicion de frecuencia cardiaca.
- Regularidad del ritmo.
- Ancho de QRS.
- Cambios ST relevantes.
- Clasificacion de riesgo.
- Mensajes de incertidumbre.

### Registro del caso

- Fecha y hora.
- Establecimiento o ubicacion opcional.
- Tipo de captura.
- Imagen original.
- Imagen procesada.
- Resultado del algoritmo.
- Observaciones del usuario.
- Conducta tomada.
- Diagnostico intrahospitalario posterior.

### Comunicacion

- Exportar PDF del caso.
- Compartir imagen y resumen por canal institucional autorizado.
- Enviar a panel web para revision.
- Integracion futura con ficha clinica o red de urgencia.

## 9. Requisitos no funcionales

- Funcionamiento rapido: idealmente resultado preliminar en menos de 30 segundos.
- Modo offline para captura y analisis basico.
- Sincronizacion diferida cuando exista conectividad.
- Cifrado de datos sensibles.
- Control de acceso por usuario.
- Registro de auditoria.
- Trazabilidad de cada interpretacion.
- Versionado de modelos de IA.
- Mensajes claros sobre limitaciones.

## 10. Arquitectura tecnica sugerida

### Aplicacion movil

Tecnologias posibles:

- Flutter, por buen rendimiento multiplataforma.
- React Native, por ecosistema amplio y desarrollo rapido.

Modulos:

- Camara guiada.
- Procesamiento local basico.
- Pantalla de resultado.
- Registro de casos.
- Sincronizacion.
- Autenticacion.

### Backend

Componentes:

- API segura.
- Base de datos de casos.
- Almacenamiento de imagenes.
- Motor de inferencia IA.
- Panel web para revision clinica.
- Modulo de reportes.

### IA y vision computacional

Componentes:

- Modelo de calidad de imagen.
- Detector de region ECG o pantalla de monitor.
- Segmentador de trazado.
- Extractor de senal.
- Clasificador de hallazgos.
- Motor de reglas clinicas para alertas.

## 11. Datos necesarios para entrenar y validar

- ECG de 12 derivaciones con diagnostico confirmado.
- Fotografias reales de ECG impresos en distintas condiciones.
- Fotografias de monitores cardiacos.
- Tiras de ritmo.
- Casos con confirmacion intrahospitalaria:
  - Troponinas o enzimas cardiacas.
  - Ecocardiograma.
  - Coronariografia si existe.
  - Diagnostico medico final.
- Etiquetas clinicas revisadas por especialistas.

## 12. Riesgos principales

- Falsos negativos en IAM o arritmias criticas.
- Falsos positivos que generen sobrecarga o traslados innecesarios.
- Mala calidad de imagen.
- Variabilidad entre monitores, papeles y formatos ECG.
- Uso fuera de protocolo.
- Responsabilidad medico-legal.
- Proteccion de datos sensibles.
- Sesgos si los datos de entrenamiento no representan poblacion rural o prehospitalaria real.

## 13. Medidas de mitigacion

- Mostrar siempre nivel de confianza.
- Bloquear interpretacion cuando la imagen sea deficiente.
- Usar lenguaje de sospecha, no de certeza diagnostica.
- Validacion clinica prospectiva antes de uso operativo.
- Auditoria medica de casos.
- Capacitacion breve dentro de la app.
- Protocolos institucionales asociados.
- Registro de version del algoritmo usado en cada caso.

## 14. Fases de desarrollo

### Fase 1: definicion y prototipo

- Definir alcance clinico.
- Crear prototipo visual.
- Validar flujo con usuarios reales.
- Definir criterios de seguridad y mensajes clinicos.

### Fase 2: MVP tecnico

- App movil con captura guiada.
- Evaluacion de calidad de imagen.
- Registro de casos.
- Analisis inicial de frecuencia, ritmo y QRS.
- Exportacion de informe.

### Fase 3: IA para ECG de 12 derivaciones

- Deteccion de derivaciones.
- Extraccion de trazado.
- Deteccion de elevacion ST.
- Clasificacion de riesgo.
- Comparacion con evaluacion medica.

### Fase 4: piloto clinico controlado

- Uso supervisado en uno o mas centros.
- Comparacion con interpretacion medica.
- Medicion de sensibilidad, especificidad y tiempos.
- Ajuste de algoritmo y mensajes.

### Fase 5: despliegue institucional

- Panel administrativo.
- Integracion con redes de urgencia.
- Capacitacion.
- Gobernanza clinica.
- Monitoreo continuo de rendimiento.

## 15. Primer MVP recomendado

El primer MVP deberia concentrarse en:

- Captura de ECG de 12 derivaciones impreso.
- Evaluacion de calidad de imagen.
- Registro del caso.
- Extraccion basica de frecuencia y regularidad.
- Deteccion preliminar de QRS ancho.
- Sospecha de supradesnivel ST solo cuando la calidad sea suficiente.
- Resultado con semaforo de riesgo.
- Campo para registrar confirmacion hospitalaria posterior.

Este alcance reduce riesgo, permite validar utilidad real y genera una base de datos propia para mejorar el modelo.

## 16. Frase de posicionamiento

Aplicacion movil de apoyo a la decision clinica para lectura asistida de ECG en escenarios prehospitalarios y rurales, orientada a priorizar casos tiempo-dependientes y facilitar la comunicacion con la red intrahospitalaria.

