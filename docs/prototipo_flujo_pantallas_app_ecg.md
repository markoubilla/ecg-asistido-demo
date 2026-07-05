# Prototipo de flujo y pantallas: app ECG prehospitalaria

## 1. Principios de diseno

La app debe ser rapida, sobria y segura. El usuario probablemente estara trabajando en un entorno con presion, ruido, mala iluminacion, guantes, poco tiempo y conectividad variable.

Prioridades:

- Pocos pasos.
- Botones grandes.
- Texto breve.
- Colores clinicos claros.
- Sin lenguaje alarmista.
- Resultado visible en menos de 30 segundos cuando sea posible.
- Opcion de guardar caso aunque no haya internet.

## 2. Navegacion principal

Pantallas principales:

1. Inicio.
2. Nueva captura.
3. Camara guiada.
4. Revision de imagen.
5. Analisis en curso.
6. Resultado.
7. Registro del caso.
8. Confirmacion intrahospitalaria.
9. Historial.

## 3. Pantalla de inicio

Objetivo: iniciar rapidamente una nueva evaluacion.

Elementos:

- Boton principal: "Nueva lectura ECG".
- Acceso secundario: "Historial".
- Indicador de conexion: "Online" / "Sin conexion".
- Usuario activo.
- Aviso breve: "Herramienta de apoyo. No reemplaza evaluacion clinica."

Acciones:

- Iniciar captura.
- Ver casos pendientes de sincronizacion.
- Abrir historial.

## 4. Pantalla: tipo de captura

Objetivo: indicar que tipo de imagen se analizara.

Opciones:

- ECG 12 derivaciones.
- Tira de ritmo.
- Monitor cardiaco.

Recomendacion para MVP:

- Activar completamente "ECG 12 derivaciones".
- Dejar "Tira de ritmo" y "Monitor cardiaco" como modos beta o fase posterior.

Texto sugerido:

"Seleccione el origen del trazado."

## 5. Pantalla: camara guiada

Objetivo: mejorar la calidad de la fotografia antes de capturar.

Elementos:

- Marco rectangular para alinear el ECG.
- Indicador de luz.
- Indicador de enfoque.
- Indicador de inclinacion.
- Boton de captura.
- Boton para activar linterna.
- Boton para cancelar.

Mensajes automaticos:

- "Acerque el ECG."
- "Evite reflejos."
- "Mantenga el papel completo dentro del marco."
- "Imagen estable."
- "Listo para capturar."

## 6. Pantalla: revision de imagen

Objetivo: permitir confirmar o repetir antes del analisis.

Elementos:

- Imagen capturada.
- Estado preliminar:
  - Buena calidad.
  - Calidad regular.
  - No interpretable.
- Boton: "Analizar".
- Boton: "Repetir foto".

Si la calidad es mala:

- Mostrar causa probable:
  - Borrosa.
  - Oscura.
  - Cortada.
  - Con reflejos.
  - Sin trazado visible.

## 7. Pantalla: analisis en curso

Objetivo: mantener informado al usuario sin saturar.

Estados:

- "Corrigiendo imagen..."
- "Detectando derivaciones..."
- "Identificando complejos QRS..."
- "Evaluando cambios criticos..."
- "Generando resultado..."

Tiempo esperado:

- Ideal: 10 a 30 segundos.
- Si tarda mas: permitir guardar y procesar en segundo plano.

## 8. Pantalla: resultado

Objetivo: mostrar hallazgos y accion sugerida de forma clara.

Estructura:

- Nivel de prioridad.
- Calidad de lectura.
- Hallazgos principales.
- Mensaje operativo.
- Botones de accion.

### Resultado rojo

Titulo:

"Alerta critica"

Subtitulo:

"Hallazgos compatibles con condicion tiempo-dependiente."

Campos:

- Calidad: Alta / Media / Baja.
- Frecuencia estimada.
- Ritmo.
- QRS.
- ST.
- Observaciones.

Acciones:

- "Guardar caso".
- "Compartir resumen".
- "Repetir ECG".
- "Agregar signos vitales".

### Resultado amarillo

Titulo:

"Requiere evaluacion"

Subtitulo:

"Hallazgos no concluyentes o potencialmente relevantes."

Acciones:

- Guardar.
- Repetir captura.
- Agregar clinica.

### Resultado verde

Titulo:

"Sin hallazgos criticos evidentes"

Subtitulo:

"No descarta patologia cardiaca. Correlacionar con clinica."

### Resultado gris

Titulo:

"No interpretable"

Subtitulo:

"La imagen no permite una lectura confiable."

Acciones:

- Repetir foto.
- Guardar imagen sin interpretacion.

## 9. Pantalla: registro del caso

Objetivo: documentar contexto clinico minimo.

Campos sugeridos:

- Edad.
- Sexo.
- Dolor toracico: si/no.
- Disnea: si/no.
- Sincope: si/no.
- Palpitaciones: si/no.
- Tiempo de sintomas.
- Presion arterial.
- Frecuencia cardiaca.
- Saturacion.
- Glasgow o estado de conciencia.
- Antecedentes relevantes.
- Conducta tomada.

Campos opcionales:

- Establecimiento.
- Unidad movil.
- Ubicacion.
- Nombre o identificador local del paciente, segun normativa institucional.

## 10. Pantalla: compartir resumen

Objetivo: comunicar rapidamente al centro receptor o regulacion.

Contenido del resumen:

- Imagen ECG.
- Resultado de la app.
- Nivel de prioridad.
- Signos vitales ingresados.
- Hora de captura.
- Usuario o unidad.
- Nota: "Interpretacion asistida, requiere confirmacion clinica."

Formatos:

- PDF.
- Imagen resumen.
- Envio a panel web institucional.

## 11. Pantalla: confirmacion intrahospitalaria

Objetivo: cerrar el ciclo diagnostico y mejorar la base de datos.

Campos:

- Diagnostico final.
- Troponina/enzimas cardiacas.
- Ecocardiograma.
- Coronariografia.
- ECG hospitalario.
- Tratamiento realizado.
- Observaciones.

Estados:

- Pendiente de confirmacion.
- Confirmado.
- Descartado.
- Sin informacion.

## 12. Pantalla: historial

Objetivo: revisar casos previos y pendientes.

Filtros:

- Fecha.
- Nivel de prioridad.
- Pendiente de sincronizar.
- Pendiente de confirmacion.
- Establecimiento.

Cada caso debe mostrar:

- Hora.
- Tipo de captura.
- Nivel de resultado.
- Estado de confirmacion.
- Estado de sincronizacion.

## 13. Flujo ideal de MVP

1. Abrir app.
2. Tocar "Nueva lectura ECG".
3. Seleccionar "ECG 12 derivaciones".
4. Tomar foto guiada.
5. Confirmar imagen.
6. Recibir resultado.
7. Agregar signos vitales minimos.
8. Guardar y compartir resumen.
9. Registrar confirmacion hospitalaria mas tarde.

## 14. Flujo de seguridad

La app debe detener o limitar resultados si:

- No se detecta ECG completo.
- La imagen esta borrosa.
- Hay reflejos que ocultan derivaciones.
- No se puede detectar escala.
- El trazado esta cortado.
- El analisis tiene baja confianza.

En esos casos debe mostrar:

"No interpretable. Repita la captura o utilice evaluacion clinica convencional."

## 15. Propuesta de menu inferior

Pestanas:

- Inicio.
- Nueva lectura.
- Historial.
- Configuracion.

## 16. Configuracion

Opciones:

- Perfil de usuario.
- Establecimiento.
- Modo offline.
- Sincronizacion.
- Exportacion de reportes.
- Protocolos locales.
- Acerca de la herramienta.

## 17. Primeras pantallas que conviene disenar visualmente

Para validar rapido con usuarios, conviene prototipar:

1. Inicio.
2. Seleccion de tipo de captura.
3. Camara guiada.
4. Revision de calidad.
5. Resultado rojo.
6. Resultado no interpretable.
7. Registro de caso.
8. Historial.

