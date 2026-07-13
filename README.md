# SAMU ECG Asistido

App web estatica de apoyo a la lectura inicial de electrocardiogramas y trazados cardiacos para personal de salud no especialista: TENS, enfermeria, medicos generales, equipos prehospitalarios, SAPU, SAR, postas rurales y servicios de urgencia.

## Alcance clinico

Esta herramienta ayuda a ordenar datos del paciente, mediciones del ECG y hallazgos visibles para entregar una orientacion de riesgo. No reemplaza criterio clinico, protocolos locales, regulacion medica, ECG formal ni evaluacion especializada.

La app no realiza diagnostico autonomo ni interpreta automaticamente una imagen con IA. La lectura actual es guiada por los datos que ingresa el usuario.

## Funciones incluidas

- Carga/captura de foto del ECG, tira de ritmo o monitor.
- Registro de contexto clinico y sintomas.
- Registro de frecuencia, PR, QRS, QT, cambios ST, ritmo y derivaciones.
- Calculo aproximado de QTc por Bazett.
- Clasificacion orientativa: rojo, amarillo, verde o no interpretable.
- Sugerencias de accion segura segun hallazgos ingresados.
- Guardado local de casos en el navegador.
- Historial local.
- Copia de resumen para compartir por canal institucional.
- Vista imprimible.
- Pauta de feedback medico.
- Estilo visual inspirado en SAMU/Chile: azul, rojo y blanco.

## Como ejecutar localmente

Abrir `index.html` directamente o levantar un servidor local:

```bash
python -m http.server 8787
```

Luego abrir:

```text
http://127.0.0.1:8787
```

## GitHub Pages

El proyecto incluye workflow en:

```text
.github/workflows/pages.yml
```

El despliegue se realiza desde la rama `gh-pages`, compatible con la configuracion actual del entorno `github-pages`.

URL esperada:

```text
https://markoubilla.github.io/ecg-asistido-demo/
```

## Netlify

El proyecto incluye:

```text
netlify.toml
```

Configuracion:

- Build command: vacio
- Publish directory: `.`

Para publicar:

1. Entrar a Netlify.
2. Importar el repositorio `markoubilla/ecg-asistido-demo`.
3. Usar la configuracion detectada desde `netlify.toml`.
4. Deploy.

## Validacion pendiente antes de uso real

- Revision por urgenciologos, cardiologos y equipos prehospitalarios.
- Validacion prospectiva con ECG reales.
- Analisis de falsos negativos y falsos positivos.
- Protocolos de uso institucional.
- Seguridad de datos y consentimiento.
- Trazabilidad y auditoria.
- Revision regulatoria/legal.

## Estado

Version funcional demostrativa para revision clinica y presentacion a futuros usuarios.

