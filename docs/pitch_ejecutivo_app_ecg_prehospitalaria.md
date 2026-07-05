# Pitch ejecutivo: app movil para lectura asistida de ECG en atencion prehospitalaria y rural

## 1. Resumen

Proponemos desarrollar una aplicacion movil de apoyo a la decision clinica para personal de atencion prehospitalaria, postas rurales, SAPU, SAR y servicios de urgencia. La app permitira capturar mediante fotografia un monitor cardiaco, una tira de ritmo o un ECG de 12 derivaciones, analizar la calidad de la imagen, extraer informacion del trazado y entregar una orientacion clinica inicial sobre hallazgos potencialmente criticos.

El objetivo no es reemplazar al medico ni emitir diagnosticos definitivos, sino apoyar la deteccion temprana, la priorizacion y la derivacion oportuna de pacientes con sospecha de eventos cardiacos tiempo-dependientes.

## 2. Problema

En atencion prehospitalaria y rural, la interpretacion de trazados cardiacos puede verse limitada por:

- Falta de especialistas disponibles en el lugar.
- Alta variabilidad en experiencia del personal.
- Equipos y formatos de ECG diferentes.
- Mala conectividad en zonas rurales.
- Presion de tiempo durante traslados o atenciones criticas.
- Dificultad para comunicar rapidamente hallazgos al centro receptor.

Esto puede retrasar decisiones como traslado prioritario, solicitud de apoyo medico, activacion de red de urgencia o confirmacion diagnostica intrahospitalaria.

## 3. Solucion propuesta

Una app movil que permita:

- Tomar una fotografia guiada del ECG o monitor.
- Corregir automaticamente perspectiva, nitidez y contraste.
- Identificar si la imagen es interpretable.
- Detectar hallazgos electrocardiograficos basicos y criticos.
- Clasificar el caso por nivel de urgencia.
- Generar un resumen clinico compartible.
- Registrar el diagnostico final confirmado en el hospital para aprendizaje y auditoria.

## 4. Usuarios beneficiados

- Personal de ambulancia.
- TENS y enfermeros/as en postas rurales.
- Equipos SAPU, SAR y urgencias.
- Medicos generales en centros de baja y mediana complejidad.
- Medicos reguladores y equipos receptores.
- Redes asistenciales que requieren mejor trazabilidad de casos cardiovasculares.

## 5. Valor diferencial

### Para el personal en terreno

- Apoyo inmediato en interpretacion de trazados.
- Mensajes claros y accionables.
- Menor incertidumbre ante ECG complejos.
- Funcionamiento movil y potencialmente offline.

### Para el sistema de salud

- Mejor priorizacion de pacientes.
- Comunicacion mas ordenada entre prehospitalaria e intrahospitalaria.
- Registro auditable del ECG inicial.
- Base de datos para mejorar protocolos y capacitacion.
- Potencial reduccion de retrasos en patologias tiempo-dependientes.

### Para el paciente

- Mayor probabilidad de deteccion temprana.
- Derivacion mas oportuna.
- Continuidad entre evaluacion inicial y confirmacion hospitalaria.

## 6. MVP propuesto

La primera version debe ser acotada, segura y validable.

Funcionalidades iniciales:

- Captura guiada de ECG de 12 derivaciones impreso.
- Evaluacion automatica de calidad de imagen.
- Registro del caso.
- Estimacion de frecuencia cardiaca.
- Deteccion de ritmo regular o irregular.
- Identificacion preliminar de QRS ancho o angosto.
- Sospecha de supradesnivel ST cuando la calidad lo permita.
- Resultado tipo semaforo: rojo, amarillo, verde o no interpretable.
- Exportacion de resumen en PDF o imagen.
- Campo para agregar diagnostico intrahospitalario posterior.

## 7. Ejemplo de resultado entregado por la app

Nivel: Rojo

Hallazgos orientativos:

- ECG interpretable.
- Frecuencia estimada: 112 lpm.
- Ritmo regular.
- QRS angosto.
- Cambios ST compatibles con posible evento isquemico agudo.

Mensaje operativo:

"Hallazgos sugerentes de patologia tiempo-dependiente. Correlacionar con clinica, signos vitales y dolor toracico. Considerar contacto con regulacion medica, repetir ECG si corresponde y traslado segun protocolo local."

## 8. Seguridad clinica

La app debe usar lenguaje prudente:

- "Sospecha de..."
- "Hallazgos compatibles con..."
- "No descarta patologia..."
- "Imagen no interpretable..."

Nunca debe presentar un resultado como diagnostico definitivo autonomo. La confirmacion debera realizarse en contexto intrahospitalario mediante evaluacion clinica, ECG formal, enzimas cardiacas, ecocardiograma, coronariografia u otros examenes segun el caso.

## 9. Desarrollo por etapas

### Etapa 1: prototipo funcional

- Diseno de pantallas.
- Flujo de captura.
- Registro basico de casos.
- Simulacion de resultado clinico.

### Etapa 2: MVP tecnico

- Procesamiento real de imagen.
- Control de calidad de captura.
- Analisis basico de trazado.
- Exportacion de informe.

### Etapa 3: validacion clinica inicial

- Comparacion contra interpretacion medica.
- Medicion de sensibilidad y especificidad en hallazgos definidos.
- Ajuste de mensajes y criterios de seguridad.

### Etapa 4: piloto institucional

- Implementacion supervisada en ambulancias, SAPU/SAR o postas.
- Revision medica de casos.
- Evaluacion de impacto en tiempos, derivaciones y comunicacion.

### Etapa 5: escalamiento

- Integracion con sistemas institucionales.
- Panel web de revision.
- Entrenamiento continuo del modelo.
- Gobernanza clinica y auditoria.

## 10. Equipo necesario

- Lider clinico de urgencia o cardiologia.
- Personal prehospitalario para validacion de flujo real.
- Desarrollador movil.
- Ingeniero backend.
- Especialista en vision computacional e IA medica.
- Experto en datos de salud y seguridad.
- Asesor regulatorio/legal.

## 11. Indicadores de exito

- Porcentaje de imagenes correctamente interpretables.
- Tiempo promedio desde captura hasta resultado.
- Sensibilidad para hallazgos criticos definidos.
- Tasa de falsos negativos en eventos relevantes.
- Concordancia con interpretacion medica.
- Tiempo de comunicacion con centro receptor.
- Satisfaccion del personal usuario.
- Porcentaje de casos con diagnostico final registrado.

## 12. Frase para presentar

"Queremos transformar el celular en una herramienta de apoyo clinico para leer ECG en terreno, priorizar pacientes cardiovasculares y conectar mejor la atencion prehospitalaria con la confirmacion intrahospitalaria."

## 13. Proxima decision

La recomendacion es avanzar con un prototipo visual navegable de la app y un flujo clinico del MVP, para validarlo con usuarios reales antes de invertir en modelos complejos de inteligencia artificial.

