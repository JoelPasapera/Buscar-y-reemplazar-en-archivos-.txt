<div align="center">

# Buscar y reemplazar en archivos `.txt`

**Una herramienta web para buscar, reemplazar y revisar texto directamente desde el navegador.**

<!-- CAMBIA ESTA URL por la dirección pública de tu aplicación. -->
<a href="https://joelpasapera.github.io/Buscar-y-reemplazar-en-archivos-.txt/" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/ABRIR%20LA%20APLICACI%C3%93N-2458D3?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Abrir la aplicación web">
</a>

<br>

![HTML](https://img.shields.io/badge/HTML5-documento-orange?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-estilos-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-sin%20frameworks-F7DF1E?logo=javascript&logoColor=222)
![Ejecución local](https://img.shields.io/badge/procesamiento-en%20el%20navegador-2E8B57)

</div>

---

## ¿Qué es?

**Buscar y reemplazar en archivos `.txt`** es una aplicación web hecha en un único archivo HTML. Permite localizar texto, revisar las coincidencias y aplicar reemplazos sin necesidad de instalar un programa ni utilizar un servidor backend.

El motor procesa el contenido por bloques para trabajar con archivos grandes. El rendimiento y el tamaño máximo práctico dependen del navegador, del equipo y de la memoria disponible; por eso, no se garantiza un tamaño máximo universal.

## Funciones principales

- **Abrir archivos:** selecciona un archivo desde el equipo o arrástralo al área de carga.
- **Buscar y reemplazar:** especifica el texto que deseas encontrar y el texto nuevo. Puedes dejar vacío el reemplazo para eliminar coincidencias.
- **Opciones de búsqueda:** distingue mayúsculas y minúsculas, busca palabras completas y permite omitir coincidencias según los caracteres que haya justo antes o después (números, letras o caracteres especiales).
- **Vista previa:** revisa el contexto de las coincidencias antes de aplicar un cambio y selecciona las coincidencias que quieres omitir.
- **Varias reglas:** pega una lista de reemplazos, una regla por línea, separando el texto buscado y el nuevo mediante una tabulación o el símbolo `→`. También puedes cargar un archivo con la lista en los formatos aceptados por el selector.
- **Navegación por líneas:** salta a una línea concreta, recorre líneas cercanas y edita una línea individual.
- **Codificaciones de texto:** admite UTF-8, Windows-1252 (ANSI), UTF-16 LE y UTF-16 BE. La aplicación intenta detectar la codificación inicial y señala cuál detectó.
- **Procesamiento cancelable:** permite detener una operación en curso.
- **Registro de cambios:** muestra las operaciones realizadas y cuántas coincidencias se modificaron; puedes quitar operaciones pendientes.
- **Guardar resultados:** descarga el archivo transformado con un nombre basado en el original y el sufijo `-reemplazado`.
- **Exportar reglas:** descarga la lista de reemplazos para reutilizarla.
- **Recuperación de la sesión:** intenta recordar la lista de cambios para el mismo archivo usando el almacenamiento local del navegador.
- **Tema claro y oscuro:** puedes elegir la apariencia de la interfaz.

## Cómo usarla

1. Abre la aplicación con el botón **ABRIR LA APLICACIÓN** de la parte superior.
2. Arrastra un archivo `.txt` al área indicada o selecciónalo desde tu equipo.
3. Escribe el texto que quieres buscar y el texto por el que deseas reemplazarlo.
4. Ajusta las opciones de búsqueda y revisa la vista previa de las coincidencias.
5. Pulsa **Aplicar cambio**. Puedes añadir más cambios y revisar el registro de operaciones.
6. Cuando hayas terminado, pulsa **Guardar archivo** para descargar el resultado. El archivo original no se sustituye automáticamente: la aplicación genera un resultado descargable.

### Lista de reemplazos

Puedes introducir varias reglas en el cuadro **Pegar una lista de cambios**. Usa una línea por regla y separa ambos campos con una tabulación o una flecha `→`:

```text
casa → hogar
perro → can
búsqueda antigua → búsqueda nueva
```

Comprueba el formato de la lista y la vista previa antes de aplicar cambios a archivos importantes.

## Codificaciones compatibles

| Codificación | Uso |
|---|---|
| UTF-8 | Texto Unicode, habitual en archivos modernos. |
| Windows-1252 (ANSI) | Archivos de texto de ciertos entornos de Windows y documentos antiguos. |
| UTF-16 LE | Texto Unicode en UTF-16, orden little-endian. |
| UTF-16 BE | Texto Unicode en UTF-16, orden big-endian. |

La codificación puede afectar qué caracteres se pueden buscar o insertar. Si el archivo tiene caracteres que no se pueden representar en la codificación seleccionada, la aplicación puede impedir ese cambio en lugar de escribir una sustitución incompatible.

## Privacidad y funcionamiento

El contenido del archivo se lee y procesa en el navegador; la aplicación no necesita subirlo a un backend para realizar los reemplazos. La lista de operaciones y la preferencia de tema pueden guardarse en el almacenamiento local del navegador para facilitar la recuperación de la sesión.

**Nota sobre recursos externos:** el HTML carga las fuentes tipográficas Atkinson desde Google Fonts. Esto significa que el navegador puede realizar solicitudes a ese servicio para obtener las fuentes. La afirmación de procesamiento local se refiere al contenido del archivo y a la lógica de búsqueda y reemplazo de la aplicación.

Como medida de precaución, conserva una copia del archivo original cuando los datos sean importantes y verifica el archivo descargado antes de utilizarlo en un proceso crítico.

## Tecnología

- **HTML** para la estructura de la aplicación.
- **CSS** para la interfaz adaptable, el tema claro/oscuro y la presentación de los resultados.
- **JavaScript** para leer archivos, detectar codificaciones, buscar coincidencias, aplicar reglas y generar el archivo de salida.
- **Blob y File API** para el procesamiento de contenido local en el navegador.
- **LocalStorage** para recordar preferencias y operaciones pendientes de recuperación.

No requiere un proceso de compilación ni un gestor de paquetes para la versión actual: la aplicación está contenida en un archivo HTML.

## Ejecutar en tu equipo

1. Descarga o clona este repositorio.
2. Abre el archivo HTML de la aplicación con un navegador moderno.
3. Selecciona un archivo de texto y empieza a trabajar.

Para publicarla en **GitHub Pages**, coloca el archivo HTML en el repositorio y configura Pages para servir desde la rama y carpeta donde lo hayas guardado. Después, reemplaza la URL de ejemplo del botón de arriba por la dirección pública de tu aplicación.

## Limitaciones a tener en cuenta

- La velocidad y el tamaño de los archivos que pueden procesarse dependen del navegador y de los recursos del equipo.
- Los archivos con contenido binario o que no sean realmente texto pueden producir resultados inesperados.
- Las funciones de selección y guardado de archivos pueden variar según el navegador y el entorno donde se abra la página.
- Antes de utilizar la aplicación con datos importantes, comprueba el resultado con una copia de prueba y confirma que la codificación y las reglas elegidas son las correctas.

---

<div align="center">

**Una herramienta ligera para transformar archivos de texto desde el navegador.**

</div>
