---
description: Guía de diagnóstico y solución cuando un DTE no se visualiza en las tablas ni en el árbol del Lector JSON.
---

# **Solución a Problemas: DTE No Aparece en el Listado**

Si descargaste o importaste un DTE y no lo visualizas en el **Lector JSON**, revisa las siguientes causas habituales de sincronización pendiente, clasificación o filtrado:

---

## **Comprobaciones Inmediatas**

### 1. Confirmar la Sincronización de Archivos
Cuando descargas comprobantes desde el correo, los archivos se almacenan temporalmente en tu carpeta de descargas. Para que los documentos se incorporen formalmente al Lector JSON:
- Es necesario que el proceso de [Sincronización](../flujos/sincronizacion.md) se haya completado con éxito.
- Si cerraste la ventana antes de finalizar o si la sincronización quedó pendiente, presiona el botón **Sincronizar** para que el sistema procese y clasifique los archivos pendientes.

---

### 2. Verificar el Periodo Fiscal (Año y Mes)
- **Fecha de emisión vs. Fecha del correo**: Si tienes activa la opción *"Usar la fecha del correo para compras"*, el DTE se ubicará en el mes en que recibiste el mensaje. De lo contrario, se clasificará según la **fecha de emisión** registrada dentro del DTE.
- Revisa los meses contiguos en el árbol lateral para verificar si fue asignado a un periodo anterior o posterior.

---

### 3. Verificar la Categoría Fiscal
Comprueba que estés explorando la rama correcta en el árbol lateral del Lector JSON:
- **Compras**: Si tu empresa figura como Receptor en el DTE (Comprobantes de Crédito Fiscal, facturas de sujeto excluido, etc.).
- **Ventas Contribuyente / Ventas Consumidor**: Si tu empresa figura como Emisor del DTE.
- **Invalidadas**: Si el documento corresponde a un evento oficial de invalidación.
- **Retornadas**: Si el documento corresponde a un evento de retorno oficial (disminución total o parcial en DTEs permisibles: **01** Factura, **11** Factura de Exportación o **14** Sujeto Excluido, con efecto similar a una nota de crédito).

---

### 4. Utilizar la Búsqueda Global
Presiona **Ctrl + F** (Windows) o **Cmd + F** (macOS) en el Lector JSON. La herramienta de búsqueda filtra en tiempo real sobre cualquiera de los valores visibles en las columnas de la tabla (Código de Generación, Número de Control, Sello, NIT, DUI, NRC, razón social o montos).

---

## **Vías de Ingreso: Descarga con Sincronización vs. Inserción Local**

Comprender cómo ingresó el DTE ayuda a ubicarlo rápidamente:

- **Vía Correo (Descarga + Sincronización)**:
  1. La **Descarga** recupera los archivos del buzón (o enlaces externos) y los deposita en la carpeta de trabajo.
  2. La **Sincronización** es el paso que valida la estructura, comprueba que el NIT corresponda a la empresa y guarda los DTEs en la base de datos. Si un archivo tiene errores de validación (por ejemplo, sin firma o en ambiente de pruebas), se notificará en los resultados de la sincronización.
- **Vía Inserción Local Directa**:
  - Al cargar archivos o carpetas desde tu disco con [Inserción Local](../flujos/importacion-json.md), los DTEs entran directamente a la base de datos sin pasar por la carpeta de descargas de correo. Si un archivo fue descartado, la causa se refleja en la columna de estado del resumen de inserción.

---

## **Soporte Adicional**
Si el DTE es válido y sigue sin aparecer en tu empresa tras verificar estos pasos, puedes contactar con nuestro equipo de asistencia técnica usando [Soporte con PIN](../suscripcion-y-soporte/solicitar-soporte-con-pin.md).