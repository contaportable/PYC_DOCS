# Parametros de Validacion

## Objetivo
Controlar reglas de inclusion y clasificacion de documentos.

## Parametros de validacion
- Inclusion de ambiente de pruebas: permite incluir documentos de ambiente de pruebas para revision y analisis 'ambiente: 00'.
- Inclusion de documentos no firmados: permite incluir documentos sin firma digital.
- Inclusion de documentos sin sello: permite incluir documentos que no tienen sello de recepción de Hacienda en el DTE (puedes tratar de recuperar el sello con la consulta en Hacienda).

# Parametros de descarga
- Usar la fecha del correo para insertar en BD(compras): al activar esta opción, el sistema usará la fecha del correo electrónico para determinar la fecha de registro en la base de datos. Esto es útil para casos donde la fecha de emisión del DTE no coincide con la fecha de recepción del correo, asegurando que los documentos se registren según la fecha en que fueron recibidos.

# Parametros configuracion
- Intervalo de consulta de DTE (segundos): define el tiempo en segundos entre cada consulta de DTE durante la sincronización. Se recomienda mantener un intervalo adecuado para evitar sobrecargar el sistema y asegurar una consulta eficiente.
- Preferencias del asistente: permite habilitar o deshabilitar los recordatorios de incorporación del asistente, facilitando la experiencia de usuario según sus necesidades y preferencias.