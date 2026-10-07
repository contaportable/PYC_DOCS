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

### **Versión 1.1.4** - 2026-10-05

- **Nuevo:**
  - **Mover Compras Masivo en Menú de Selección Múltiple**: Posibilidad de seleccionar uno o múltiples DTEs de compras (Comprobante de Crédito Fiscal) y trasladarlos a otro periodo fiscal dentro de la ventana legal de 3 meses permitida por el Código Tributario de El Salvador para deducir compras.
  - **Control de Ventana Única por Empresa**: Prevención de duplicación de ventanas de una misma empresa; al intentar abrir una empresa que ya está en uso, el sistema enfoca y trae al frente la ventana activa existente.
  - **Protección contra Eliminación Accidental**: Bloqueo preventivo que impide eliminar una empresa si tiene ventanas abiertas o tareas activas en ejecución.

- **Mejorado:**
  - **Gestión de Errores en Traslados**: Notificación detallada indicando la cantidad de DTEs trasladados exitosamente y advertencias cuando el periodo fiscal de destino se encuentra bloqueado.
  - **Validación de Selección Múltiple**: Guardas de seguridad al ejecutar acciones de eliminación con múltiples registros seleccionados en tablas.

- **Corregido:**
  - Corrección en la persistencia y actualización del listado de DTEs pendientes con eventos de retorno.
  - Ajuste en la sincronización de etiquetas tras consultas individuales o masivas de DTEs.

- **Impacto Operativo:**
  - Flexibilidad contable para diferir compras de Crédito Fiscal a periodos fiscales posteriores dentro del plazo legalmente autorizado.
  - Mayor seguridad operativa al evitar colisiones e inconsistencias de datos por apertura duplicada de ventanas.

---

### **Versión 1.1.3** - 2026-10-02

- **Nuevo:**
  - **Soporte Avanzado de Factura de Exportación (FEXE 11)**: Tratamiento y categorización inteligente de facturas de exportación en importaciones e internaciones, con actualización del catálogo de países para compatibilidad con códigos de versiones anteriores.
  - **Ventana de Progreso y Bloqueo Dinámico de Interfaz**: Incorporación de indicador de progreso visual que desactiva temporalmente las acciones durante procesos asíncronos para evitar ejecuciones accidentales.
  - **Restablecer Tamaño de Columnas**: Opción en el menú contextual de tablas para restaurar instantáneamente el ancho predeterminado de las columnas tras modificaciones manuales.

- **Mejorado:**
  - **Maquetación Continua en PDF**: Optimización de saltos de página y diseño continuo en PDF para Facturas de Exportación extensas, evitando resúmenes o firmas huérfanas al final del documento.
  - **Prioridad de Columnas Críticas**: Optimización del ancho y visibilidad preferente para el número de control y código de generación en las tablas.

- **Corregido:**
  - Corrección en la asignación de campos para tributos e impuestos en DTEs.
  - Prevención de desbordamientos visuales en diálogos informativos al utilizar fuentes de gran tamaño.

- **Impacto Operativo:**
  - Conciliación y registro confiable de operaciones de exportación bajo la normativa tributaria vigente.
  - Experiencia visual estable y mayor control sobre las vistas de datos en tablas extensas.

---

### **Versión 1.1.2** - 2026-09-16

- **Nuevo:**
  - **Desglose Independiente de NRC y NIT**: Separación explícita de los campos de NRC y NIT en columnas dedicadas tanto en la tabla visual como en las exportaciones a Excel, sustituyendo la columna única anterior de identificación.
  - **Almacenamiento Local Seguro**: Mecanismo de guardado con archivos temporales y protección ante cortes de energía o cierres imprevistos, previniendo la corrupción de los registros locales.

- **Mejorado:**
  - **Persistencia de Metadatos de Anexos**: Inicialización y resguardo de datos auxiliares para declaraciones tributarias.

- **Corregido:**
  - Corrección de anomalías causadas por caracteres nulos o formatos no válidos en archivos JSON importados.

- **Impacto Operativo:**
  - Identificación inmediata de contribuyentes y simplificación en cruces contables gracias al desglose individual de NRC y NIT.
  - Máxima fiabilidad en el almacenamiento local de DTEs y registros fiscales.

---

### **Versión 1.1.1** - 2026-09-09

- **Nuevo:**
  - **Protección y Bloqueo de Periodos Fiscales**: Restricción de acciones modificadoras (inserción, consulta o eliminación) en periodos fiscales cerrados, junto con un diálogo de confirmación interactiva para autorizar su desbloqueo.
  - **Consulta Inteligente en el Servicio de Hacienda**: Descarte automático en consultas masivas de DTEs que ya fueron validados previamente o que cuentan con evento de invalidación, optimizando el tiempo de respuesta.
  - **Consulta Selectiva de DTEs**: Posibilidad de seleccionar varios DTEs y consultar su estado en el Ministerio de Hacienda directamente desde el menú contextual.
  - **Apertura Directa por Doble Clic**: Doble clic sobre cualquier fila de la tabla para visualizar el DTE en modo PDF por defecto.
  - **Descarga Directa desde Menú Contextual**: Acción para descargar y ubicar el archivo del DTE seleccionado en el equipo.

- **Mejorado:**
  - **Escalabilidad Visual y Fuentes Adaptativas**: Ajuste dinámico de diálogos, tablas y botones para tamaños de letra grandes (hasta 20 puntos) sin truncamiento de información.
  - **Diseño de Libros de IVA en Excel**: Formato y anchos de columna adaptados para evitar saltos del código de generación, con totalizadores dinámicos optimizados.
  - **Independencia del Entorno**: Estandarización de textos y mensajes operativos con independencia del idioma o configuración regional del sistema operativo.
  - **Compatibilidad con macOS**: Optimización en la navegación entre periodos fiscales y centrado geométrico de diálogos modales.

- **Corregido:**
  - Corrección en la idempotencia del estado de bloqueo de periodo frente a consultas de estado.
  - Prevención de excepciones en tablas al interactuar con filas deseleccionadas o selecciones vacías.

- **Impacto Operativo:**
  - Blindaje de la información contable contra modificaciones accidentales en periodos ya declarados.
  - Consultas tributarias ágiles y eficientes sin saturar el servicio de consulta del Ministerio de Hacienda.

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
