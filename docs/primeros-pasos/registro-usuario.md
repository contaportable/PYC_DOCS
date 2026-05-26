# Registro de Usuario

## Objetivo
Crear y activar la cuenta de usuario que permitirá iniciar sesión en PyConta.

## Antes de empezar
- Tener conexión a internet.
- Disponer de una dirección de correo válida para el registro.
- Preparar las capturas del flujo completo de registro para documentar cada paso.

## Flujo de registro de usuario

### 1) Configuración de cuenta
En esta sección se configura la base del usuario y parámetros de operación.

Índice rápido de este paso:
- Parámetros de validaciones de contraseña y reglas activas.
- Regla **"Usar la fecha del correo para insertar en BD"** (activar solo cuando aplique al flujo del cliente).
- Intervalo de consulta de DTE (segundos): definir un rango operativo estable.
- Preferencias del asistente: habilitar o deshabilitar recordatorios de incorporación.

![Configuración de cuenta](../assets/img/primeros-pasos/registro-usuario-01-configuracion-cuenta.png "Configuración de cuenta y parámetros iniciales"){ align=center }

### 2) Preguntas de seguridad
Estas preguntas deben ser seguras y fáciles de recordar para el titular de la cuenta.

!!! warning "Importante"
	Este será el único método de verificación para recuperación de acceso.
	Las respuestas deben resguardarse en un medio interno seguro y con acceso restringido.

![Preguntas de seguridad](../assets/img/primeros-pasos/registro-usuario-02-preguntas-seguridad.png "Preguntas de seguridad para recuperación"){ align=center }

### 3) Configuración de descargas
Aquí se define la ruta donde se descargarán los DTE.

- Por defecto, la ruta corresponde a la ubicación de instalación.
- Si el cliente lo requiere, se puede cambiar a otra ruta autorizada.
- Si el usuario necesita los DTE sueltos en esa carpeta, debe activar **"Exportar descargas sin cifrado"**.

![Configuración de descargas](../assets/img/primeros-pasos/registro-usuario-03-configuracion-descargas.png "Ruta de descarga y exportación sin cifrado"){ align=center }

### 4) Datos personales
Completar los campos obligatorios con información real y vigente.

- Validar nombres y apellidos.
- Registrar un correo real de uso del usuario.
- Verificar formato de fecha y datos de contacto.

![Datos personales](../assets/img/primeros-pasos/registro-usuario-04-datos-personales.png "Campos obligatorios de datos personales"){ align=center }

### 5) Llenar ubicación
Completar la ubicación y dirección según los datos reales de la empresa o del usuario.

- País, departamento, municipio y distrito.
- Dirección exacta para mantener consistencia documental.

![Ubicación según empresa](../assets/img/primeros-pasos/registro-usuario-05-ubicacion-empresa.png "Ubicación del usuario según empresa"){ align=center }

### 6) Extra: configuración de fuente
Opcionalmente, se puede ajustar la fuente para mejorar legibilidad según preferencia del usuario.

![Configuración de fuente](../assets/img/primeros-pasos/registro-usuario-06-configuracion-fuente.png "Ajuste opcional de tipografía"){ align=center }

### Confirmación de registro
Al finalizar el formulario, guardar cambios y confirmar el mensaje de éxito.

![Usuario registrado con éxito](../assets/img/primeros-pasos/registro-usuario-07-registro-exitoso.png "Confirmación final de registro"){ align=center }

## Verificación
- Ingresar sin error y visualizar el panel principal.
- Comprobar versión en "Acerca de" (muestra plan y límites).

## Errores frecuentes
- Correo ya registrado: usar recuperación de contraseña o contactar soporte.
- No llega correo de verificación: revisar spam y filtros.

## Diferencias Demo vs Plan pago
- PyConta0: no se solicita clave de activación; límites reducidos aplican automáticamente (ver "Acerca de").
- Plan pago: tras ingresar la clave de activación el usuario obtiene los límites y permisos del plan contratado.

## Relacionados
- [Instalación, Acceso y Requisitos](instalacion-acceso.md)
- [Licencias y Planes](licencias-y-planes.md)
