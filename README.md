# Aplicaciones de generación de documentación de FFEs

Aplicaciones web para preparar documentación de la Fase de Formación en Empresa y firmar
documentos PDF. Están orientadas principalmente a su uso dentro de un
Aula Virtual de Educamadrid, basada en Moodle.

Las aplicaciones procesan los archivos en el navegador. No se envían a un
servidor de este proyecto. Para cargar las librerías externas y, en el caso de
la firma, comunicarse con AutoFirma, se necesita conexión a Internet.

## Aplicaciones

| Aplicación | Descripción | Página standalone | Fragmento para Moodle |
|---|---|---|---|
| Anexo I · Acceso a FFE | Genera los anexos de acceso a FFE del alumnado. | [Abrir](https://javpalacios.github.io/herramientas-ffe/standalone/anexo-i-acceso.html) | [Código Moodle](anexo-i-acceso/anexo-i-acceso-moodle.html) |
| Anexo I · Plan de formación | Prepara el plan de formación y sus resultados de aprendizaje. | [Abrir](https://javpalacios.github.io/herramientas-ffe/standalone/anexo-i-plan-formacion.html) | [Código Moodle](anexo-i-plan-formacion/anexo-i-plan-formacion-moodle.html) |
| Firma masiva de ficheros PDF | Firma varios PDF con la misma ubicación de firma. | [Abrir](https://javpalacios.github.io/herramientas-ffe/standalone/firma-cualquier-archivo.html) | [Código Moodle](firma-cualquier-archivo/firma-cualquier-archivo-moodle.html) |

## Uso recomendado en Aula Virtual de Educamadrid

Se recomienda utilizar la versión **Moodle** de cada aplicación:

1. En el curso, activa la edición y añade un recurso de tipo **Página**.
2. Abre el archivo `*-moodle.html` de la aplicación elegida y copia todo su
   contenido. En el editor WYSIWYG de Moodle, selecciona **Contenido → Ver →
   Código fuente**, pega allí el código y confirma los cambios.
3. Guarda la página y comprueba que la aplicación se carga y que sus botones
   funcionan.

La aplicación **Anexo I · Plan de formación** puede personalizarse para cada
centro. En el código de la aplicación, modifica los valores de `DEFAULTS`
(centro, correo y teléfono del centro, tutor/a y sus datos de contacto) para que
aparezcan cumplimentados por defecto al abrirla. Después, copia y guarda en
Moodle la versión modificada.

La ejecución de JavaScript en páginas Moodle puede depender de la configuración
del sitio, los permisos de la cuenta y los filtros de contenido. Si Moodle
elimina o bloquea los scripts, la aplicación puede no funcionar incrustada.

## Alternativa: versión standalone

Si la versión Moodle no funciona por las restricciones de JavaScript, utiliza
la versión **standalone** alojada en GitHub Pages:

1. Añade al curso un recurso de tipo **URL**.
2. Pega la dirección de la aplicación standalone. Las páginas están en la
   carpeta [`standalone/`](standalone/); por ejemplo:
   `https://javpalacios.github.io/herramientas-ffe/standalone/anexo-i-acceso.html`.
3. En **Apariencia → Mostrar**, selecciona **En una ventana emergente** o
   **Incrustar**, según el resultado que prefieras.
4. Guarda y prueba el enlace con una cuenta de estudiante.

También puedes probar las aplicaciones desde la
[página principal de GitHub Pages](https://javpalacios.github.io/herramientas-ffe/).

Las páginas standalone reutilizan los mismos fragmentos de aplicación que las
versiones Moodle, dentro de un marco, y cargan Bootstrap para su presentación.
Así se evita mantener dos implementaciones de la lógica. La publicación
standalone requiere que GitHub Pages esté habilitado para el repositorio.

## Requisitos para firmar PDF

La aplicación de firma requiere que AutoFirma esté instalada y disponible en el
dispositivo. La firma se realiza mediante el componente AutoScript y puede
requerir que el navegador permita la comunicación con AutoFirma.

## Aviso de uso

El autor no se hace responsable del uso indebido de estas aplicaciones ni de
los problemas derivados de modificaciones del código realizadas por terceros.
El software se ofrece sin garantías, en los términos de la licencia aplicable y
sin perjuicio de los derechos o responsabilidades que no puedan excluirse
legalmente. Antes de utilizar los documentos generados, revisa que los datos y
el resultado sean correctos.

## Licencia

Este proyecto se distribuye bajo la licencia **GNU General Public License,
versión 3 o, a elección del usuario, cualquier versión posterior**
(GPL-3.0-or-later). Consulta [`LICENSE`](LICENSE) y el
[texto oficial de la licencia](https://www.gnu.org/licenses/gpl-3.0.html).

Las bibliotecas de terceros cargadas por las aplicaciones conservan sus
propias licencias y condiciones.
