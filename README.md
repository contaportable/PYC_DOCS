# PYC_DOCS

Documentación pública de PyConta, pensada para contadores, administradores y usuarios operativos que necesitan aprender el producto rápido y resolver tareas del día a día sin leer código.

## Que es PyConta

PyConta es un software de escritorio desarrollado en Python que automatiza el procesamiento de Facturas Electronicas (DTE).

Permite descargar DTE desde correo, validar y clasificar documentos por contribuyente, periodo y tipo, y organizar la informacion en una base estructurada lista para el trabajo contable.

## Funciones principales

- Creacion de Usuario.
- Configuracion de Usuario.
- Vista de Administracion de Empresas.
- Gestion de Empresas.
- Lector JSON.
- Mostrar DTE en vista grafica y lectura JSON/PDF.
- Descargar archivos JSON desde correo electronico.
- Sincronizar correo.
- Importar JSON desde carpeta local.
- Generar CSV de anexos.
- Extraer a Excel.
- Categorizacion de DTEs.
- Consulta de estado de DTE en Ministerio de Hacienda.
- Parametros de validacion.
- Extraccion de DTEs para analisis.
- Generacion de archivo de metadata para procesamiento de IA.
- Autocompletado inteligente para columnas ISR del anexo F07.
- Predicciones globales para columnas ISR del anexo F07(compras).
- Anexos de Impuestos F07.

## Objetivo de este repositorio

Este repositorio documenta el uso real de PyConta desde la perspectiva del usuario final.

La prioridad es responder tres preguntas:

- Que hace PyConta.
- Como se usa PyConta.
- Que hacer cuando algo falla.

## Enfoque editorial

- Lenguaje claro y operativo.
- Pocas vueltas, pasos directos y verificables.
- Contenido organizado por tareas, no por tecnicismos.
- Espacios reservados para capturas en los puntos donde el usuario necesita orientacion visual.

## Secciones de la documentacion

- Primeros pasos: acceso, configuracion y puesta en marcha.
- Flujo de trabajo: descarga, importacion, validacion, consulta y exportacion (incluye Gestión de Empresas y Lector JSON).
- Informacion importante: limites, requisitos y buenas practicas.
- Problemas comunes: sintomas, causas y solucion rapida.
- Suscripcion y soporte: vigencia, renovacion, upgrade y asistencia remota.
- Politicas: redencion y devolucion.
- FAQ y glosario: respuestas breves y terminos clave.
- Novedades: actualizaciones, mejoras y cambios importantes.
## Estructura base

- `docs/primeros-pasos/`
- `docs/flujos/`
- `docs/informacion-importante/`
- `docs/problemas-comunes/`
- `docs/suscripcion-y-soporte/`
- `docs/politicas/`
- `docs/faq-glosario/`
- `docs/novedades/`
- `docs/assets/img/`

## Convencion de imagenes

- Formato recomendado: `png`.
- Nombre recomendado: `seccion-tema-paso-contexto.png`.
- Rutas por tipo:
   - `docs/assets/img/flujos/`
   - `docs/assets/img/modulos/`
   - `docs/assets/img/incidencias/`
   - `docs/assets/img/soporte/`

## Acceso rapido a la documentacion local

Si levantas el sitio con Docker, la documentacion queda disponible en:

http://localhost:8008/PYC_DOCS/

<!--
INSTRUCCIONES DE DESPLIEGUE LOCAL CON DOCKER:

1) Requisitos:
   - Tener instalado Docker y Docker Compose (CLI v2).

2) Confirmar puerto en `docker-compose.yml`:
   - Asegurarse de que el servicio `mkdocs` expone el puerto `8008:8000`.

3) Levantar el servicio en segundo plano:
   docker compose up -d

4) Ver logs (si necesitás depurar):
   docker compose logs -f mkdocs

5) Acceder a la documentación en:
   http://localhost:8008/PYC_DOCS/

6) Detener y remover contenedores:
   docker compose down

Notas:
- `mkdocs.yml` usa `site_dir: site/PYC_DOCS`; si cambias el path base actualiza `site_url` según corresponda.
- Si prefieres otro puerto, modifica la parte izquierda de la entrada `ports` en `docker-compose.yml`.
-->