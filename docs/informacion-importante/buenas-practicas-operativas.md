---
description: Recomendaciones y buenas prácticas para la operación segura, ordenada y eficiente de PyConta.
---

# **Buenas Prácticas Operativas**

A continuación se presentan las pautas y recomendaciones clave para optimizar el uso de **PyConta**, asegurar la correcta captura de documentos y agilizar la generación de libros de IVA y declaraciones tributarias.

---

## 1. Operación en Despachos con Múltiples Empresas
Cuando administras varias empresas utilizando una misma cuenta de correo principal, se recomienda organizar el flujo mediante carpetas o etiquetas desde tu proveedor de correo (webmail):

1. **Crear reglas en el correo**: Enruta los mensajes de cada empresa hacia carpetas o etiquetas específicas.
2. **Asignar carpetas en PyConta**: Configura cada empresa en PyConta para que lea únicamente su carpeta o buzón asignado.
3. **Evitar carpetas compartidas**: No utilices una sola carpeta general para múltiples empresas con el fin de evitar cruces de información y facilitar la conciliación.

---

## 2. Consulta de DTEs antes de Generar Anexos y Libros
Antes de cerrar el periodo y generar tus Anexos F07 o Libros de IVA, realiza la consulta oficial de DTEs ante el servicio de consulta del Ministerio de Hacienda:

- **Detectar DTEs Invalidados o Retornados**: Identifica a tiempo cualquier DTE que haya sido invalidado o sujeto a eventos de retorno.
- **Recuperar Sellos Faltantes**: Asegura que los documentos recibidos en contingencia incorporen su sello oficial de recepción.
- **Verificar Observaciones**: Revisa cualquier notificación tributaria registrada antes de proceder con las salidas finales.

---

## 3. Configuración y Reglas de Descarga por Correo
Para optimizar el proceso de descarga y reducir intervenciones manuales, verifica los siguientes puntos en la configuración:

- **Tipos de DTE a procesar**: Verifica que estén activados únicamente los tipos de DTE deseados (Compras y/o Ventas) según el rol de la cuenta vinculada.
- **Buzones y carpetas activas**: Comprueba que los buzones o etiquetas donde se reciben las facturas se encuentren debidamente marcados.
- **Extracción de DTEs desde enlaces**: Si cuentas con proveedores que envían enlaces web en lugar de adjuntar directamente el archivo `.json` o los `.pdf`, configura los remitentes correspondientes para habilitar la extracción automática de DTEs desde enlaces externos seguros.

### Servidores de Correo Personalizados (IMAP)
Para servidores de correo corporativos o personalizados, valida previamente los parámetros de conexión requeridos:
- Servidor IMAP (host)
- Puerto y método de cifrado (SSL/TLS)
- Credenciales / contraseña (por lo general la autenticación usa la misma contraseña del correo)

## 4. Resguardo de Preguntas de Seguridad
Las preguntas de seguridad son el mecanismo principal para la recuperación de tu usuario en caso de olvido de credenciales:

- Resguarda las preguntas y respuestas en un gestor o medio seguro interno.
- Utiliza respuestas claras y precisas que puedas recordar fácilmente.
- Limita el acceso a esta información únicamente al personal administrativo autorizado.

!!! warning "Importante"
    Si se extravían las respuestas a las preguntas de seguridad, la recuperación del acceso a tu usuario no será posible.

---

## 5. Gestión de Archivos en la Carpeta de Trabajo
Evita mover, renombrar o eliminar manualmente los archivos dentro de las carpetas internas de descarga mientras PyConta se encuentra en ejecución:

- Utiliza las funciones de **Extraer DTEs** o **Exportar a Excel** desde el **Lector JSON** para generar copias en tus carpetas personales de trabajo.
- Conserva la estructura de directorios generada por el sistema para garantizar la trazabilidad y sincronización continua.

---

## 6. Primera Descarga en Planes Premium
Al activar una cuenta en un Plan Premium, dispones de una descarga inicial sugerida con un rango amplio (por ejemplo, 1 año) para construir tu historial base:

- Planifica la primera descarga para capturar todo el periodo histórico que necesites conciliar.
- Tras la primera sincronización, el sistema recordará el historial y sugerirá automáticamente los periodos pendientes en las descargas sucesivas.

---

## **Checklist Rápido de Operación Mensual**
1. Confirmar que las cuentas de correo y carpetas asignadas a la empresa estén activas.
2. Ejecutar la descarga del periodo y realizar la sincronización en el Lector JSON.
3. Consultar el estado de los DTEs ante el servicio de consulta de Hacienda para validar sellos y vigencia.
4. Revisar el resumen financiero y corroborar compras y ventas en el panel principal.
5. Exportar los Libros de IVA en formato Excel y PDF.
6. Preparar y validar la tabla de Anexos de Impuestos F07 antes de generar el archivo CSV oficial.

---

## **Enlaces Relacionados**
- [Descarga Desde Correo](../flujos/descarga-desde-correo.md)
- [Lector JSON](../flujos/lector-json.md)
- [Consulta en Hacienda](../flujos/consulta-hacienda.md)
- [Generación de Libros de IVA](../flujos/libros-iva.md)
- [Anexos de Impuestos F07](../flujos/anexos-de-impuestos-f07.md)

---

## **Guías Externas para Reglas en Webmail**
- **Microsoft Outlook:** [Administrar mensajes mediante reglas en Outlook](https://support.microsoft.com/es-es/office/administrar-mensajes-de-correo-electr%C3%B3nico-mediante-reglas-en-outlook-c24f5dea-9465-4df4-ad17-a50704d66c59)
- **Google Gmail:** [Crear reglas para filtrar correos en Gmail](https://support.google.com/mail/answer/6579?hl=es)
- **Yahoo Mail:** [Configuración de filtros y reglas en Yahoo Mail](https://es.ayuda.yahoo.com/kb/SLN28071.html)
