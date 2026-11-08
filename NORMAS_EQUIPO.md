# NORMAS DE EQUIPO

## 1. Gestión del proyecto en GitHub

Todo el trabajo del proyecto se organizará y gestionará mediante GitHub, utilizando un repositorio común y un único GitHub Project.

### 1.1. Gestión de tareas mediante Issues
- Cada tarea del proyecto deberá tener su correspondiente Issue en GitHub.
- Los Issues seguirán la nomenclatura establecida: `[ASIGNATURA]-[NUMERO]-[NombreSinEspacios]`.
- Se utilizarán dos cifras para numerar las tareas y códigos de asignatura en mayúsculas.
- Cada Issue deberá incluir una descripción clara del trabajo que se debe realizar, las tareas principales y el entregable correspondiente.



## 2. Estrategia de ramas (Git)

Se utilizará Git para controlar las versiones del proyecto y permitir que varios integrantes trabajen simultáneamente sin interferir directamente en el código de los demás.

### 2.1. Ramas principales
Se trabajará con dos ramas principales:

- **main:** contendrá las versiones estables del proyecto. No se realizarán cambios directamente sobre ella.
- **dev:** será la rama principal de desarrollo y contendrá los cambios que hayan sido revisados e integrados.

Ningún integrante deberá realizar commits directamente sobre estas ramas.

### 2.2. Ramas de trabajo
Cada tarea deberá desarrollarse en su propia rama, creada a partir de `dev`.

Se utilizará el siguiente formato:

`<ASIGNATURA>-<NUMERO>_<tema>`

Ejemplos:
- `DWES-04_publicaciones`
- `DWEC-01_feed`
- `DIW-02_accesibilidad`

Las ramas deberán estar relacionadas con el Issue correspondiente.



## 3. Reglas de commits

Los commits deberán seguir el formato de **Conventional Commits**:

`<tipo>(<ámbito>): <descripción>`

### 3.1. Tipos de commits
Se utilizarán los siguientes tipos:

- `feat`: incorporación de una nueva funcionalidad.
- `fix`: corrección de errores.
- `docs`: cambios en la documentación.
- `style`: cambios de formato o presentación que no modifican la lógica.
- `refactor`: reorganización o mejora del código sin cambiar su comportamiento.
- `test`: incorporación o modificación de pruebas.
- `chore`: tareas de mantenimiento y configuración.

### 3.2. Ejemplos
- `feat(perfiles): implementar edición de perfiles`
- `fix(publicaciones): corregir visualización de imágenes`
- `docs(modelo-er): actualizar diagrama de entidades`
- `style(feed): ajustar diseño responsive`
- `refactor(compras): separar lógica del carrito`
- `chore(config): actualizar configuración del proyecto`


## 4. Revisión de código

Las revisiones deben ser aprobadas por al menos otro integrante. También, se debe comprobar que cumple con los requisitos del profesorado y con este documento, en el que se especifican las reglas de equipo.

## 5. Organización del código y estructura del repositorio

El repositorio seguirá una estructura común para mantener separados los diferentes módulos y facilitar el trabajo de todos los integrantes.

Se respetará la estructura de carpetas establecida para el proyecto:



- `red-social/`: desarrollo de la red social, con backend en PHP, frontend en JavaScript y base de datos.
- `compra-venta/`: módulos de compras y ventas.
- `infraestructura/`: recursos de infraestructura relacionados con DAW.
- `data-analytics/`: datasets, notebooks, visualizaciones e informes de análisis de datos.
- `diseno/`: archivos de Figma, guía de estilos y recursos de accesibilidad.
- `documentacion/`: documentación técnica organizada por asignatura o área.


## 6. Reglas de desarrollo

Todos los integrantes deberán mantener un estilo de desarrollo coherente y respetar las tecnologías y responsabilidades de cada módulo.

### 6.1. HTML
- Se utilizará HTML semántico siempre que sea posible.
- Se emplearán correctamente elementos como `header`, `nav`, `main`, `section`, `article` y `footer`.
- Se mantendrá una jerarquía lógica de encabezados.
- Las imágenes deberán incluir textos alternativos (`alt`) cuando corresponda.

### 6.2. CSS
- Se evitarán los estilos directamente en los elementos HTML.
- Las clases utilizarán nomenclatura `kebab-case`.
- Se priorizará el uso de variables CSS para colores, tamaños y otros valores reutilizables.
- Se aplicará una metodología Mobile First.
- Se priorizarán unidades relativas cuando sean adecuadas.
- Se evitarán duplicaciones innecesarias de estilos.

### 6.3. JavaScript
- Se utilizarán nombres descriptivos para variables, funciones y constantes.
- Se separarán las responsabilidades para evitar funciones demasiado extensas.
- Se evitará duplicar código cuando pueda reutilizarse.
- Se controlarán los errores y respuestas de las peticiones a las APIs.
- Se utilizará el almacenamiento local únicamente cuando corresponda a la funcionalidad requerida.

### 6.4. PHP
- Se separará la lógica de negocio del acceso a datos y de la presentación.
- Se utilizarán consultas preparadas para interactuar con la base de datos.
- Se validarán los datos recibidos antes de procesarlos.
- Las contraseñas se almacenarán mediante funciones seguras de hash.
- Se evitará repetir lógica que pueda centralizarse o reutilizarse.

### 6.5. Java / Jakarta EE
- Los módulos de Compras y Ventas mantendrán separadas sus responsabilidades.
- Se organizará el código de manera coherente, evitando mezclar lógica de presentación, negocio y persistencia.
- Se gestionarán adecuadamente las excepciones.
- Se evitará duplicar funcionalidades o lógica entre módulos.
- Se respetará la integración con la base de datos compartida.

## 7. Base de datos e integración entre módulos

La base de datos será un elemento compartido por las aplicaciones del proyecto, por lo que es importante avisar a los compañeros de cualquier tipo de cambio. Debemos seguir y actualizar el modelo entidad-relación.

## 8. Uso de GitHub Copilot

- Al utilizar GitHub Copilot, se le indicará que siga estas normas de equipo y las reglas aplicables al proyecto.
- El código y los cambios propuestos por Copilot deberán revisarse antes de integrarlos.
- Si un commit se realiza con ayuda de Copilot, el autor deberá ser únicamente el integrante que realiza el commit, usando su identidad Git configurada. Copilot no figurará como autor ni como coautor.