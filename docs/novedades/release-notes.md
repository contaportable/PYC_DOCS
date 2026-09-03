---
description: Historial de actualizaciones, mejoras operativas y nuevas funcionalidades incorporadas en cada versión de PyConta.
---

# **Novedades y Release Notes**

En esta página se registran los cambios funcionales, mejoras operativas y nuevas características incorporadas en las diferentes versiones de **PyConta**.

<!--
### Versión X.Y.Z - AAAA-MM-DD
- **Nuevo:**
- **Mejorado:**
- **Corregido:**
- **Impacto operativo:**
- **Acciones recomendadas:**
-->

---

### **Versión 1.1.0.0**

- **Nuevo:**
  - **Visor Estandarizado y Conmutador PDF / JSON**: Apertura homogénea de DTEs desde la carga de archivos, visualización directa en PDF y alternancia instantánea a la estructura de datos JSON.
  - **Eventos de Retorno e Invalidadas**: Gestión completa para eventos de retorno (disminución contable en DTEs 01, 11 y 14) y eventos de invalidación con control de periodos fiscales cerrados.
  - **Libros de IVA con Tablas Secundarias**: Exportación con fórmulas dinámicas y estilos avanzados en Excel, diseño continuo en PDF y restricción de marcas de agua para planes Demo.
  - **Asignación Automática de DUI**: Reconocimiento y ubicación automática del DUI en su columna correspondiente para Anexos F07 y libros de IVA.
  - **Consulta en Hacienda Integrada**: Validación implícita durante sincronización/inserción y recuperación inteligente de sellos desde la metadata.
  - **Normativa 2.0 y Contingencia**: Compatibilidad integral con esquemas v2 (Sujeto Excluido tipo 14, retenciones, percepciones, autoconsumos) y soporte para DTEs en contingencia.
  - **Extracción de Archivos Comprimidos**: Soporte ampliado en descarga de correos para archivos, `.zip`, `.rar`, `.7z`, documentos `.txt` y gestión de enlaces externos seguros.
  - **Preferencias y Estados Visuales**: Configuración de abreviaturas para códigos de control, panel de preferencias y sistema de estados con emojis informativos en tablas.

- **Mejorado:**
  - **Rendimiento e Inserción Masiva**: Procesamiento por lotes fluido sin saturación de la interfaz gráfica y algoritmo de ordenamiento por fecha, hora y correlativo.
  - **Edición en Anexos Tributarios**: Mayor precisión en la edición y visualización de columnas de NIT, NRC y DUI en modelos de Anexos F07.
  - **Autenticación y Conectividad OAuth2**: Flujo renovado para cuentas de correo con cambio dinámico de credenciales y renovación de tokens.
  - **Seguridad y Registro**: Empaquetado optimizado con control defensivo de ventanas y sistema de logs adaptativo según el entorno.

- **Corregido:**
  - Corrección en la clasificación de DTEs y cálculo de totales en tablas secundarias de libros de IVA.
  - Corrección en el tratamiento de valores negativos para notas de crédito en los libros de IVA.
  - Exclusión estricta de DTEs invalidados en todas las secciones de los Anexos F07.
  - Corrección en la captura y cálculo de retenciones de IVA del 1% y 13% en anexos.
  - Corrección de reconexión para clientes IMAP / Gmail API y prevención de conflictos multisesión.
  - Manejo defensivo de conversiones numéricas y caracteres especiales en DTEs.
  - Prevención de bloqueos durante la actualización del sistema mediante bloqueos de ejecución (*locks*).

- **Impacto Operativo:**
  - Flujo contable continuo con visualización gráfica en PDF y alternancia técnica a JSON.
  - Automatización total en el tratamiento de retornos, invalidaciones y normativa tributaria 2.0.
  - Mayor precisión y calidad profesional en la exportación de libros de IVA y Anexos F07.

---

### **Versión 1.0.0.9.4**

- **Nuevo:**
  - **Descarga Inteligente por Cuenta**: Detección automática del último mes descargado y sugerencia del periodo pendiente en el panel de descargas.
  - **Precarga de 1 Año en Descarga Inicial**: Sugerencia de un rango anual en la primera conexión de una cuenta para construir el historial completo.
  - **Validación en Bloque de Anexos**: Verificación automática de datos y formato antes de generar los archivos finales de declaración F07.
  - **Reutilización de Cupos de Correo**: Flexibilidad para actualizar o cambiar cuentas de correo manteniendo el cupo asignado a la empresa.

- **Mejorado:**
  - Mensajes de validación y orientación visual más claros durante el registro de usuarios y empresas.
  - Rendimiento y estabilidad al extraer DTEs desde archivos comprimidos.

- **Corregido:**
  - Corrección de cálculo en valores de retenciones y percepciones en tablas secundarias de anexos.
  - Mejora en la captura de logs operativos para soporte técnico asistido.

---

### **Versión 1.0.0.9.3**

- **Nuevo:**
  - Implementación de la primera sincronización inteligente para lectura de historial descargado.
  - Integración de filtros de búsqueda avanzados en el panel de inserción manual.
  - Flujo guiado de bienvenida (*onboarding*) para nuevos usuarios.
  - Paneles redimensionables en la pantalla de carga de archivos.

- **Mejorado:**
  - Optimización en el motor de búsqueda del visor de DTEs y carga progresiva por lotes.
  - Transiciones y velocidad visual en formularios de empresas y usuarios.
  - Mejoras en el algoritmo de limpieza y codificación de archivos JSON.
  - Autocompletado de operaciones de ventas a consumidores y facturas de exportación en la tabla de Anexos F07.

- **Corregido:**
  - Corrección en sumatorias automáticas en columnas de totales de Anexos F07.
  - Corrección de comportamiento al usar Deshacer (Ctrl + Z) en el registro de ventas del anexo.
