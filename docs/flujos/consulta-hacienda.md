---
description: Procedimiento para la verificación del estado oficial de DTEs directamente ante el servicio de consulta del Ministerio de Hacienda en PyConta.
---

# **Consulta en Hacienda**

PyConta te permite verificar en tiempo real el estado tributario oficial de tus DTEs directamente contra el servicio de consulta del **Ministerio de Hacienda**, asegurando la validez fiscal y la trazabilidad de tus operaciones.

---

## **Beneficios de la Consulta Oficial**

Al consultar tus DTEs ante el Ministerio de Hacienda, obtienes:

- **Validación de Estado Oficial**: Confirmación de si el documento está *Aceptado*, *Rechazado*, *Invalidado* o *Ajustado*.
- **Recuperación de Sello de Recepción**: Si recibiste un DTE en contingencia o sin sello visible, la consulta oficial lo recupera e incorpora automáticamente al documento.
- **Detección de Observaciones**: Registro de cualquier observación o mensaje emitido por la autoridad tributaria.
- **Protección de Datos**: Los documentos consultados conservan su trazabilidad oficial y quedan protegidos contra sobreescrituras accidentales en futuras importaciones.

---

## **Modalidades de Consulta en PyConta**

### 1. Consulta Individual
Ideal para validar un documento puntual desde el menú contextual o las acciones del listado:

1. Haz clic derecho sobre el DTE en la tabla.
2. Selecciona la opción **Consultar DTE en Hacienda** (o **Consultar DTE**).
3. El sistema consultará el estado y actualizará los datos del DTE al instante.

![Consulta individual de DTE](../assets/img/flujos/consulta-hacienda-01-consulta-individual.png "Consulta individual desde acciones del DTE"){ align=center }

---

### 2. Consulta Masiva Inteligente por Categoría
Permite validar todos los DTEs de un periodo (Compras o Ventas) en un solo proceso:

1. Selecciona la categoría del periodo en el árbol lateral.
2. Presiona el botón de **Consulta Masiva en Hacienda**.
3. **Optimización Inteligente y Descarte Preventivo**: El sistema detecta y omite automáticamente los documentos que ya cuentan con validación oficial previa, así como aquellos que registran eventos oficiales de invalidación o eventos de retorno. Esto evita reconsultas innecesarias, acelera significativamente el tiempo de procesamiento y previene la saturación del servicio de consulta del Ministerio de Hacienda.

![Consulta masiva - inicio](../assets/img/flujos/consulta-hacienda-02-consulta-masiva-inicio.png "Ejecución de consulta masiva por categoría"){ align=center }

Al finalizar el proceso, se presenta un panel detallado con el resumen de estados:

![Consulta masiva - resultado](../assets/img/flujos/consulta-hacienda-03-consulta-masiva-resultado.png "Resultados de la consulta masiva en Hacienda"){ align=center }

---

### 3. Consulta de Filas Seleccionadas
Si necesitas verificar el estado tributario de un grupo específico de documentos sin procesar toda la categoría:

1. Marca las filas deseadas en la tabla utilizando ++shift++ o ++ctrl++ para selección continua o alterna.
2. Haz clic derecho sobre cualquiera de las filas marcadas.
3. Selecciona la opción **Consultar DTEs (seleccionados)**.
4. El sistema procesará exclusivamente los documentos indicados, actualizando su sello y estado en pantalla.

![Consulta de filas seleccionadas](../assets/img/flujos/consulta-hacienda-seleccionados.png "Opción para consultar DTEs seleccionados en el menú contextual"){ align=center }

!!! note "Protección en Periodos Bloqueados"
    Si el periodo fiscal consultado se encuentra bloqueado (cerrado contablemente), el sistema restringe la ejecución de consultas que modifiquen la metadata de los documentos para preservar la integridad histórica. Para consultar documentos en un periodo protegido, este debe ser desbloqueado previamente con confirmación interactiva.

---

## **Trazabilidad y Resguardo del Estado Oficial**

Una vez realizada la consulta, la información devuelta por el Ministerio de Hacienda (fecha de consulta, estado tributario, sello oficial y observaciones) queda vinculada al DTE:

- Se refleja en la columna de estado del listado.
- Queda integrada en la vista PDF y JSON del documento.
- Los documentos validados quedan protegidos para evitar reprocesamientos innecesarios al sincronizar nuevamente.

![Metadata mh_status en JSON](../assets/img/flujos/consulta-hacienda-04-metadata-mh-status.png "Estado oficial registrado en el DTE"){ align=center }

---

## **Enlaces Relacionados**
- [Lector JSON](lector-json.md)
- [Solución a Problemas: DTE Sin Sello](../problemas-comunes/dte-sin-sello.md)
- [Solución a Problemas: DTE No Aparece](../problemas-comunes/dte-no-aparece.md)
