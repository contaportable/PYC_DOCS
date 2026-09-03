---
description: Configuración de parámetros de validación, reglas de descarga y preferencias operativas en PyConta.
---

# **Parámetros de Validación y Configuración**

PyConta ofrece opciones de configuración para adaptar el procesamiento, las reglas de validación y la descarga de documentos tributarios a las necesidades operativas de tu empresa.

---

## **Reglas de Validación de Documentos**

Estas opciones determinan qué DTEs deben ser aceptados o filtrados al importar y sincronizar:

- **Inclusión de ambiente de pruebas**: Permite admitir documentos emitidos en ambiente de pruebas (`ambiente: 00`) para fines de capacitación o análisis previo al paso a producción.
- **Inclusión de documentos no firmados**: Controla si se procesan DTEs que carecen de firma digital.
- **Inclusión de documentos sin sello**: Permite ingresar DTEs que no traen el sello de recepción visible (útil para posteriormente recuperar el sello oficial mediante la **Consulta DTE**).

---

## **Parámetros de Descarga**

- **Usar fecha del correo para compras**: Al activar esta opción, el sistema registra el DTE en la base de datos utilizando la fecha en que se recibió el correo electrónico en lugar de la fecha de emisión del DTE. Esto resulta muy útil cuando un proveedor envía una factura días después de su emisión y necesitas que compute en el mes contable de recepción.

---

## **Parámetros de Rendimiento y Experiencia**

- **Intervalo de consulta en Hacienda**: Define el tiempo de espera (en segundos) entre cada petición durante consultas masivas para mantener una comunicación fluida y respetuosa con el servicio de consulta del Ministerio de Hacienda.
- **Preferencias del asistente de bienvenida**: Permite habilitar o deshabilitar las guías iniciales de incorporación (*onboarding*) según tu nivel de familiaridad con el sistema.

---

## **Enlaces Relacionados**
- [Descarga Desde Correo](descarga-desde-correo.md)
- [Consulta en Hacienda](consulta-hacienda.md)
- [Buenas Prácticas Operativas](../informacion-importante/buenas-practicas-operativas.md)