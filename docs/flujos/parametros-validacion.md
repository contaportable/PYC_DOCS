---
description: Configuración de parámetros de validación, reglas de descarga y preferencias operativas en PyConta.
---

# **Parámetros de Validación y Configuración**

PyConta ofrece opciones de configuración para adaptar el procesamiento, las reglas de validación y la descarga de documentos tributarios a las necesidades operativas de tu empresa.

---

## **Reglas de Validación de Documentos**

Estas opciones determinan qué DTEs deben ser aceptados o filtrados al importar y sincronizar:

- **Corrección inteligente de IVA (DTEs con inconsistencias)**: Permite la admisión tolerante de DTEs emitidos por proveedores cuyos sistemas de facturación redondean o calculan el IVA con diferencias menores respecto a la base imponible legal (13%). Al activarse, PyConta admite el documento asignándole el estado de advertencia preventiva (`⚠️`), preservando el cálculo legal y permitiendo su registro sin detener las inserciones masivas.
- **Inclusión de ambiente de pruebas**: Permite admitir documentos emitidos en ambiente de pruebas (`ambiente: 00`) para fines de capacitación o análisis previo al paso a producción.
- **Inclusión de documentos no firmados**: Controla si se procesan DTEs que carecen de firma digital.
- **Inclusión de documentos sin sello**: Permite ingresar DTEs que no traen el sello de recepción visible (útil para posteriormente recuperar el sello oficial mediante la **Consulta DTE en Hacienda**).

---

## **Estados de Validación Operativa de DTEs**

Al procesar e importar DTEs en PyConta, cada documento se clasifica bajo un estado operativo:

| Estado | Ícono | Descripción | Acción Recomendada |
| :--- | :---: | :--- | :--- |
| **Válido / Conforme** | :material-check-circle: | Cumple estrictamente con el esquema tributario y la validación matemática. | Operación normal. |
| **DTE con Inconsistencias** | ⚠️ | Admitido por tolerancia con anomalías menores (IVA reconstruido, sello no visible o firma recuperada). | Consultar en Hacienda o inspeccionar motivo en el menú contextual. |
| **Rechazado** | :material-close-circle: | Estructura JSON corrupta, NIT emisor incompatible o documento no perteneciente al periodo. | Verificar archivo original con el emisor. |

!!! note "Transparencia Tributaria"
    Los DTEs marcados con advertencia (`⚠️`) pueden ser consultados en cualquier momento ante el Ministerio de Hacienda para obtener su estatus definitivo y recuperar su sello de recepción oficial.

---

## **Parámetros de Descarga**

- **Usar fecha del correo para compras**: Al activar esta opción, el sistema registra el DTE en la base de datos utilizando la fecha en que se recibió el correo electrónico en lugar de la fecha de emisión del DTE. Esto resulta muy útil cuando un proveedor envía una factura días después de su emisión y necesitas que compute en el mes contable de recepción.

---

## **Parámetros de Rendimiento y Experiencia**

- **Intervalo de consulta en Hacienda**: Define el tiempo de espera (en segundos) entre cada petición durante consultas masivas para mantener una comunicación fluida y respetuosa con el servicio de consulta del Ministerio de Hacienda.
- **Preferencias del asistente de bienvenida**: Permite habilitar o deshabilitar las guías iniciales de incorporación (*onboarding*) según tu nivel de familiaridad con el sistema.

---

## **Enlaces Relacionados**
- [Bitácora de Actividades](bitacora-actividades.md)
- [Descarga Desde Correo](descarga-desde-correo.md)
- [Lector JSON](lector-json.md)
- [Consulta en Hacienda](consulta-hacienda.md)
- [Buenas Prácticas Operativas](../informacion-importante/buenas-practicas-operativas.md)