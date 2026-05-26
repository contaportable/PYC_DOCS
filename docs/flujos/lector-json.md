# Lector JSON

## Objetivo
Gestionar, consultar y extraer DTE ya cargados en el sistema desde un panel centralizado.

## Funcionalidades del modulo

### 1) Separacion por estructura (anio, mes y categorias)
El arbol lateral permite navegar por anio, mes y categorias:

- Compras
- Otras Compras
- Ventas Contribuyentes
- Ventas Consumidor

![Separación por año, mes y categorías](../assets/img/flujos/lector-json-01-separacion-anio-mes-categorias.png "Navegación por año, mes y categorías"){ align=center }

### 2) Resumenes graficos personalizables
El apartado de resumen muestra analisis visual mensual y anual. Puede configurarse para incluir o descartar DTE segun reglas de analisis.

![Resumen gráfico personalizable](../assets/img/flujos/lector-json-02-resumen-grafico.png "Resumen financiero con configuración gráfica"){ align=center }

### 3) Menú Contextual para consultar DTE y acciones disponibles
Desde el menu contextual donde se listan las opciones de consulta y acciones para cada DTE:

![Consulta de DTE y acciones](../assets/img/flujos/lector-json-03-consultar-dte-y-acciones.png "Menú de acciones para consultar DTE"){ align=center }

### 4) Eliminar DTE
La opcion **Eliminar** permite retirar registros seleccionados cuando se requiera depuracion.

### 5) Buscar DTE
La barra de busqueda permite filtrar por datos clave para ubicar rapidamente documentos.

![Buscar DTE](../assets/img/flujos/lector-json-05-buscar-dte.png "Búsqueda y filtrado de DTE"){ align=center }

### 6) Mostrar DTE (alternado JSON y PDF)
El visor permite alternar entre modo JSON y modo PDF para revisar contenido tecnico y representacion visual del documento.

![Vista detallada en JSON](../assets/img/flujos/lector-json-06-vista-detallada-modo-json.png "Vista detallada en modo JSON"){ align=center }

![Vista detallada en PDF](../assets/img/flujos/lector-json-04-vista-detallada-modo-pdf.png "Vista detallada en modo PDF"){ align=center }

### 7) Generar CSV
Permite exportar informacion tabular para trabajo contable y revision externa.

![Generar CSV](../assets/img/flujos/lector-json-07-generar-csv.png "Opción de generación de CSV"){ align=center }

### 8) Abrir Archivo
La opcion **Abrir Archivo** abre el documento fuente en el sistema operativo.

### 9) Extraer DTEs
Permite extraer DTE por periodos disponibles en el arbol (mes o anio).

![Extraer DTEs](../assets/img/flujos/lector-json-08-extraer-dtes.png "Extracción de DTE por período"){ align=center }

### 10) Extraer Excel
Permite generar salida Excel por periodo para analisis financiero.

![Extraer Excel](../assets/img/flujos/lector-json-09-extraer-excel.png "Extracción a Excel por período"){ align=center }

### 11) Extraer seleccionados
Desde la seleccion de filas, se puede extraer un subconjunto especifico de DTE/Excel.

![Extraer seleccionados](../assets/img/flujos/lector-json-10-extraer-seleccionados.png "Extracción de elementos seleccionados"){ align=center }

### 12) Mover DTE
Permite mover un DTE a otro periodo (anio/mes) cuando se requiere reclasificacion.

![Mover DTE](../assets/img/flujos/lector-json-11-mover-dte.png "Movimiento de DTE entre períodos"){ align=center }

## Extra util
### Exportar metadatos
Adicionalmente, el sistema permite exportar metadatos por anio y mes.

![Exportar metadatos](../assets/img/flujos/lector-json-12-exportar-metadatos.png "Exportación de metadatos por año/mes"){ align=center }

## Verificacion
- El arbol de periodos y categorias refleja la estructura esperada.
- Las consultas, busqueda y visualizacion JSON/PDF responden correctamente.
- Las salidas CSV/Excel y extracciones se generan en el destino esperado.
