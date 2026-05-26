# Buenas Practicas Operativas

## Objetivo
Definir practicas recomendadas para operar PyConta de forma segura, ordenada y eficiente, minimizando errores en descarga, validacion y generacion de anexos.

## 1) Operacion en despachos con multiples empresas
Cuando un despacho administra varias empresas desde un mismo correo, se recomienda separar el flujo por buzones o carpetas desde el webmail.

### Recomendacion
1. Crear reglas en el webmail para enrutar correos de cada empresa a carpetas especificas.
2. En PyConta, configurar cada empresa para que lea unicamente su carpeta asignada.
3. Evitar usar una sola carpeta general para todas las empresas.

### Beneficio
- Reduce cruces de documentos entre empresas.
- Mejora la trazabilidad de cada descarga.
- Disminuye errores de clasificacion.

## 2) Consulta de DTE antes de generar anexos
Antes de generar anexos, ejecutar la consulta de DTE para detectar estados relevantes.

### Verificar especialmente
- DTE ajustado.
- DTE invalidado.
- Observaciones relevantes en el estado del documento.

### Recomendacion operativa
1. Ejecutar consulta de DTE por el periodo a reportar.
2. Corregir o depurar casos observados.
3. Generar anexos solo cuando el lote este validado.

## 3) Uso de reglas de descarga por correo
Configurar reglas de descarga por correo para automatizar la captura y reducir intervencion manual.

### Recomendacion
- Definir reglas por remitente, asunto o patron util.
- Mantener reglas simples y auditables.
- Revisar periodicamente reglas obsoletas o duplicadas.

### Servidores de correo personalizados
Para servidores de correo personalizados, es estrictamente importante validar los requisitos de conexión antes de configurar la descarga automatizada:
- Servidor IMAP (host)
- Puerto y método de cifrado (SSL/TLS)
- Credenciales / contraseña (por lo general la autenticación usa la misma contraseña del correo)

## 4) Resguardo de preguntas de seguridad
Las preguntas de seguridad son el mecanismo principal para recuperar el usuario.

### Recomendacion critica
- Resguardar preguntas y respuestas en un medio seguro interno del despacho.
- Evitar respuestas ambiguas o que puedan olvidarse.
- Limitar acceso a esta informacion solo a personal autorizado.

!!! warning "Importante"
    Si se pierden las respuestas de seguridad, la recuperacion del usuario puede quedar bloqueada.

## 5) Gestion correcta de archivos en Downloads
No mover manualmente archivos de la carpeta Downloads utilizada por PyConta durante el flujo normal.

### Si necesitas extraer archivos
- Usar extraccion individual desde Lector JSON.
- Usar extraccion masiva desde Lector JSON.
- Conservar intacta la estructura de trabajo usada para sincronizacion y trazabilidad.

## Checklist rapido de operacion
1. Confirmar reglas de correo activas por empresa.
2. Verificar carpeta asignada por empresa en PyConta.
3. Ejecutar consulta de DTE antes de anexos.
4. Revisar estados ajustado/invalidado/observaciones.
5. Generar anexos solo con lote validado.
6. No mover archivos de Downloads fuera del flujo.

## 6) Primera descarga ilimitada (Planes premium)

Si tu suscripción corresponde a un plan premium, dispones de una primera descarga ilimitada: puedes descargar todos los DTE dentro del rango de fechas que necesites sin que se consuma tu cuota. El consumo de los límites del plan comenzará a contabilizarse a partir de la descarga siguiente a esa operación inicial.

### Recomendación
- Planificar la primera descarga para incluir todo el histórico o el rango necesario al activar el plan.
- Verificar la integridad y clasificación después de esa descarga inicial y antes de generar anexos.
- Tener en cuenta que cualquier descarga posterior consumirá cuota según lo definido por el plan.

## Relacionados
- [Descarga Desde Correo](../flujos/descarga-desde-correo.md)
- [Consulta en Hacienda](../flujos/consulta-hacienda.md)
- [Lector JSON](../flujos/lector-json.md)
- [Licencias y Planes](../primeros-pasos/licencias-y-planes.md)

## Enlaces útiles para reglas de descarga en webmails con proveedores comunes

- **Outlook:** [Administrar mensajes y reglas en Outlook](https://support.microsoft.com/es-es/office/administrar-mensajes-de-correo-electr%C3%B3nico-mediante-reglas-en-outlook-c24f5dea-9465-4df4-ad17-a50704d66c59)
- **Gmail:** [Filtros y reglas en Gmail](https://support.google.com/mail/answer/6579?hl=es)
- **Yahoo:** [Reglas de filtrado en Yahoo Mail](https://es.ayuda.yahoo.com/kb/SLN28071.html)
