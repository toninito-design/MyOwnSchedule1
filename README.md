# Cuaderno de Bitácora · v7

Publicación en GitHub Pages: sustituye el index.html anterior por el incluido en este paquete. No requiere instalación ni compilación. Conserva la misma dirección de publicación, navegador y perfil para mantener automáticamente los datos locales. Exporta una copia JSON antes de actualizar; si cambias de dirección o navegador, impórtala después.

## Novedades

- Botón + en cada cuadrante: abre el formulario con ese cuadrante seleccionado.
- Subtareas: botones Editar y Eliminar junto a la fecha, con edición del nombre y la fecha, cancelación y confirmación al borrar. Disponibles también en Vista general.
- Pestaña Registro reuniones con Nueva reunión y Registro de reuniones.
- Modelo basado en el acta facilitada: nombre, fecha, hora, lugar, curso lectivo, departamento/comisión, convoca, modalidad, número de acta, notas, acuerdos y seguimiento, temas pendientes, asistentes y cierre. Se incluyen seis filas iniciales de acuerdos, seis de temas pendientes y ocho de asistentes; se pueden añadir o eliminar filas.
- Las reuniones se guardan automáticamente al escribir. El listado muestra nombre, fecha y curso; pulsa una reunión para abrirla y editarla. Una reunión sin nombre aparece como borrador.
- Cada acuerdo permite abrir el formulario habitual de tareas con el texto, área Reuniones, responsable y fecha límite preparados. Selecciona el cuadrante y completa los demás datos antes de guardar. Si eliges Delegar, el responsable se ofrece en su selector. Las siguientes pulsaciones abren la tarea vinculada, sin duplicarla. El acta y la tarea conservan sus propios textos y estados: editarlos no modifica automáticamente el otro registro.
- Eliminar una reunión o una fila no elimina las tareas trasladadas al planificador.

## PDF e impresión

Abre una reunión, indica su nombre y pulsa Descargar PDF / Imprimir. En la ventana de impresión puedes imprimir o seleccionar Guardar como PDF. Se genera una vista del acta con sus tablas y notas completas, sin botones ni formularios. La función utiliza el navegador y no necesita servicios externos.

## Datos y copias de seguridad

Se mantiene la clave local jvs-agenda-estrategica-v1, así como tareas, subtareas, rutinas y su historial. Las reuniones se añaden al campo meetings de los nuevos backups JSON. Se conserva el formato de copia versión 1, ampliado con ese campo opcional.

Los backups anteriores siguen siendo importables. Al importar una copia sin meetings, se reemplazan las tareas y rutinas de esa copia y se conservan las reuniones actuales; la confirmación lo indica. Una copia que sí contiene meetings reemplaza también el registro de reuniones, incluidas listas vacías. Exporta siempre una copia actual antes de reemplazar datos. Para conservar reuniones utiliza esta versión o posteriores; una versión antigua de la web no conoce ese campo.

Se conservan las mejoras de v6: nombre Cuaderno de Bitácora, Vista general en segunda posición, tareas completadas ocultas de los cuadrantes y archivadas en el listado con filtros, recuperación al desmarcar, eliminación confirmada de tareas finalizadas desde Vista general y compatibilidad JSON.

Se mantienen las demás funciones de v5, incluida la importación anual CSV/Excel. La importación Excel conserva la biblioteca XLSX del CDN original y necesita conexión.

## Comprobaciones realizadas

Pruebas funcionales en Microsoft Edge con datos ficticios aislados: creación desde los cuatro cuadrantes; edición y eliminación de subtareas en cuadrantes y calendario; cancelaciones; creación, edición, autosave, listado y reapertura de reuniones; filas adicionales; traslado de acuerdos y reapertura de tareas vinculadas sin duplicados; impresión y vista para PDF; exportación e importación JSON antigua/nueva con reuniones; conservación tras recargar; borrado de reuniones conservando tareas; visualización móvil de 390 px y revisión visual de la vista de impresión. Sin errores JavaScript en los recorridos comprobados.

También se han repetido las pruebas de v6 para archivado, filtros, recuperación, eliminación cancelada/confirmada desde Vista general, rutinas, subtareas y backups. No se ha publicado ni modificado ningún repositorio remoto.
