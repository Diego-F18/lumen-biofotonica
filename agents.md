# Reglas de trabajo del proyecto Lumen-Biofotonica

## Alcance y estructura

- El proyecto es una pagina estatica sin framework: `index.html` contiene la estructura y el contenido, `style.css` la presentacion y `script.js` la interactividad.
- Mantener los recursos principales en la raiz. Los archivos nuevos deben colocarse en carpetas descriptivas solo cuando aporten organizacion real.
- Actualizar `README.md` cuando cambien las instrucciones de ejecucion, la estructura o las tecnologias principales.
- Conservar la licencia MIT y sus avisos de copyright.

## HTML

- Usar HTML5 semantico: `header`, `nav`, `main`, `section`, `article`, `aside` y `footer` segun corresponda.
- Mantener un unico `h1` por pagina y una jerarquia logica de encabezados.
- Conservar textos alternativos significativos, etiquetas de formulario y atributos ARIA solo cuando aporten informacion que HTML no proporciona.
- Usar enlaces internos relativos a los identificadores de seccion y revisar que cada `id` sea unico.
- Evitar HTML generado con JavaScript cuando el contenido pueda declararse directamente en el documento.
- Mantener los comentarios de seccion breves y utiles para identificar bloques grandes.
- Validar que las etiquetas tengan cierre correcto y que no existan atributos duplicados.

## CSS

- Mantener la paleta y las fuentes mediante variables CSS declaradas en `:root`; reutilizar `--navy`, `--ivory`, `--red`, `--slate` y las variables tipograficas existentes.
- Organizar las reglas por secciones, siguiendo el orden funcional del proyecto y usando comentarios solo para separar bloques principales.
- Preferir clases reutilizables y selectores simples. Evitar selectores demasiado largos o acoplamiento innecesario a elementos internos.
- Usar `box-sizing: border-box`, flexbox o grid segun corresponda y conservar el diseno adaptable mediante las consultas `@media` existentes.
- No introducir valores arbitrarios duplicados si existe una variable de espaciado, color, sombra o transicion apropiada.
- Verificar estados `hover`, `focus-visible`, `active` y `prefers-reduced-motion`.
- Evitar declaraciones vacias, propiedades duplicadas, valores CSS desconocidos y abreviaciones que sobrescriban propiedades sin querer.

## JavaScript

- Mantener `script.js` sin codigo global innecesario y seguir el patron modular actual de funciones `init...`.
- Comenzar la ejecucion desde `DOMContentLoaded` y comprobar que los elementos requeridos existan antes de registrarlos o modificarlos.
- Usar `const` y `let`; evitar variables globales, ejecucion fuera de contexto y transformaciones sin causa clara.
- Mantener actualizados los atributos ARIA cuando JavaScript cambie estado visual o controles interactivos.
- Usar nombres descriptivos en ingles o espanol de forma consistente y preferir funciones pequenas con una responsabilidad.
- Limpiar observadores o listeners solo cuando exista una posibilidad real de ciclo de vida del componente; no duplicar listeners.
- Validar datos provenientes de inputs con rangos y conversiones explicitas antes de usarlos en calculos o renderizado.
- No bloquear el hilo principal con trabajo costoso; para Canvas, separar calculo, actualizacion de DOM y dibujado cuando sea posible.
- Evitar `innerHTML`; preferir APIs DOM seguras si se necesita contenido dinamico.

## Accesibilidad y experiencia

- Todo control interactivo debe ser accesible por teclado y tener un indicador de foco visible.
- Mantener contrastes suficientes entre texto, fondos y estados activos.
- Respetar `prefers-reduced-motion` y no depender solo de animaciones para comunicar cambios.
- Las visualizaciones educativas deben indicar su naturaleza conceptual y su finalidad informativa.
- Las referencias cientificas deben conservar una redaccion cautelosa y separar claramente datos conocidos de modelos o estimaciones.

## Calidad y verificaciones

- Antes de entregar cambios: revisar el diff, conservar formato consistente y no modificar archivos ajenos a la tarea.
- Verificar que los identificadores referenciados existan y que los enlaces internos no apunten a secciones inexistentes.
- Ejecutar al menos las comprobaciones disponibles para HTML, CSS y JavaScript.
- No introducir errores de sintaxis ni dependencias sin documentarlas en `README.md`.
- Las publicaciones deben preservar el funcionamiento responsive en escritorio, tablet y movil.
