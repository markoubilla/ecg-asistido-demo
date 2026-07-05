# ECG Asistido - demo prehospitalaria

Prototipo funcional navegable de una aplicacion movil para lectura asistida de trazados cardiacos en contexto prehospitalario, rural y de urgencia.

La demo esta pensada para recoger opinion de medicos, equipos de urgencia, personal prehospitalario, postas rurales, SAPU, SAR y posibles socios tecnicos.

## Importante

Este prototipo no analiza ECG reales, no usa inteligencia artificial real y no entrega diagnosticos medicos. Simula el flujo de trabajo, la experiencia de usuario, los mensajes de seguridad y la forma en que podria registrarse una sospecha inicial para posterior confirmacion intrahospitalaria.

Uso previsto de esta version:

- Validar si el flujo es util en terreno.
- Revisar lenguaje clinico y mensajes de seguridad.
- Evaluar si las pantallas son claras para personal de urgencia.
- Recoger observaciones antes de construir un MVP tecnico real.

No debe utilizarse para tomar decisiones clinicas reales.

## Como probar la demo

Abrir directamente:

```text
index.html
```

O levantar un servidor local desde esta carpeta:

```bash
python -m http.server 8787
```

Luego abrir:

```text
http://127.0.0.1:8787
```

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub.
2. Subir todos los archivos de esta carpeta.
3. Ir a `Settings` -> `Pages`.
4. En `Build and deployment`, seleccionar:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Guardar.
6. GitHub entregara una URL publica para mostrar la demo.

## Flujo incluido

La demo permite recorrer:

1. Inicio.
2. Nueva lectura ECG.
3. Seleccion de tipo de captura.
4. Camara guiada simulada.
5. Revision de calidad de imagen.
6. Analisis simulado.
7. Resultado critico.
8. Resultado no interpretable.
9. Registro clinico minimo.
10. Resumen para compartir.
11. Historial.
12. Confirmacion intrahospitalaria.

## Simulaciones disponibles

En el panel lateral se puede alternar entre:

- `ECG interpretable`: simula una captura suficiente y muestra una alerta critica.
- `Forzar mala imagen`: simula una foto deficiente y muestra resultado no interpretable.

## Preguntas sugeridas para revision medica

- El flujo es realista para atencion prehospitalaria o rural?
- Los textos son clinicamente prudentes?
- El resultado tipo semaforo es util o podria inducir errores?
- Que hallazgos deberia priorizar el MVP?
- Que datos clinicos minimos faltan?
- Que mensajes deberian cambiarse antes de una prueba piloto?
- En que escenarios no deberia usarse la aplicacion?

## Documentos incluidos

La carpeta `docs/` incluye:

- Especificacion inicial del proyecto.
- Pitch ejecutivo.
- Flujo de pantallas del prototipo.

## Proximos pasos tecnicos

Una vez validado con usuarios clinicos, el siguiente paso seria construir un MVP real con:

- App movil en Flutter o React Native.
- Captura real de camara.
- Control de calidad de imagen.
- Backend seguro.
- Registro auditable de casos.
- Validacion clinica supervisada.
- Modelo de vision computacional entrenado y evaluado con datos reales.

## Estado

Demo conceptual, no clinica, no diagnostica.

