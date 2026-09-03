---
description: Guía de diagnóstico y solución cuando PyConta no descarga correos o DTEs desde las bandejas configuradas.
---

# **Solución a Problemas: No Descarga Correos**

Si al ejecutar el proceso de descarga notas que no se obtienen nuevos DTEs desde tu cuenta de correo vinculada o que ciertos documentos no ingresan al sistema, revisa las siguientes causas y pasos de diagnóstico.

---

## **Causas Frecuentes y Diagnóstico**

| Causa Probable | Verificación Recomendada |
|---|---|
| **Permisos de acceso OAuth expirados o revocados** | Vuelve a iniciar sesión con tu proveedor (Google o Microsoft) para renovar los permisos de lectura de la cuenta. |
| **Bandeja o carpeta no seleccionada** | Comprueba que la carpeta correspondiente esté marcada en las reglas de selección de buzones. |
| **Rango de fechas fuera del periodo esperado** | Asegúrate de que el selector de periodo incluya la fecha en que se recibieron los correos con los DTEs. |
| **Correos con enlaces web sin regla de extracción** | Si el proveedor envía botones o enlaces de descarga web, asegúrate de activar la regla de **Extracción Avanzada** para ese remitente. |
| **DTEs omitidos por parámetros de validación** | Documentos filtrados por venir sin sello, no firmados o en ambiente de pruebas según las reglas activas. |
| **Acceso IMAP deshabilitado (Cuentas IMAP)** | Si usas un servidor corporativo personalizado, verifica que el protocolo IMAP esté activo en tu proveedor de correo. |
| **Archivos en Spam o Correo no deseado** | Si el mensaje fue catalogado como correo no deseado por tu servidor, muévelo a la Bandeja de Entrada para que PyConta pueda leerlo. |

---

## **Procedimiento de Solución Paso a Paso**

### 1. Reautenticar la Cuenta de Correo
1. Ve a la vista de **Empresas** y selecciona tu empresa.
2. En la sección de **Cuentas de Correo**, haz clic nuevamente en **"Iniciar Sesión con Google"** o **"Iniciar Sesión con Microsoft"** según tu proveedor.
3. Concede los permisos de lectura solicitados en el navegador para renovar la conexión.

---

### 2. Verificar Reglas de Descarga y Fechas
1. En el panel de descarga, confirma que los tipos de DTE deseados (Compras o Ventas) se encuentren activados.
2. Si prefieres definir un rango de fechas libre o amplio, selecciona el modo **Personalizado** y establece el intervalo deseado.

---

### 3. Verificar Formato de Adjuntos y Enlaces Externos
- **Archivos adjuntos compatibles**: Asegúrate de que los correos recibidos contengan los DTEs en formato directo `.json` o dentro de paquetes comprimidos compatibles (`.zip`, `.rar`, `.7z`).
- **Descargas desde enlaces**: Si el proveedor no adjunta directamente el archivo sino que incluye un enlace o botón web de descarga (como ocurre con empresas de servicios o telecomunicaciones), configura dicho remitente en la sección de [Extracción Avanzada](../flujos/descarga-desde-correo.md#3-extraccion-avanzada) con la opción **Procesar enlaces externos** habilitada.

---

### 4. Revisar DTEs con Errores y Parámetros de Validación
Al finalizar la descarga, examina la lista de resultados y el contador de archivos **Con Errores** o **Descartados**:

1. **Identificar la causa del error**: Puedes hacer clic derecho sobre la fila y usar **Abrir Archivo** o consultar la consola para verificar el motivo del rechazo.
2. **Evaluar si es un error de validación**:
   - **Documento sin sello de recepción**: El emisor envió el documento en contingencia o antes de ser procesado por el servicio de Hacienda.
   - **Documento no firmado**: El DTE carece de la firma digital requerida.
   - **Ambiente de pruebas (`00`)**: El comprobante fue generado en un entorno no productivo.
3. **Determinar la acción a seguir**:
   - **Ajustar tus preferencias**: Si deseas admitir estos documentos para su revisión contable y posterior regularización de sellos mediante la consulta en Hacienda, puedes habilitar su ingreso desde los [Parámetros de Validación](../flujos/parametros-validacion.md).
   - **Reclamar al emisor**: Si consideras que el documento incumple las normativas fiscales y no debe procesarse con anomalías, comunícate directamente con el proveedor o emisor de la factura para que subsane el problema y reenvíe un DTE válido y firmado.

---

## **¿El problema persiste?**
Si tras seguir estos pasos la descarga no se completa, solicita asistencia técnica mediante [Soporte con PIN](../suscripcion-y-soporte/solicitar-soporte-con-pin.md).