# diw-flexbox1-plata-moran-carlos
Git Hub que contendra todo de la carpeta de la Practica 4 para el Ejercicio 4: CSS 2: Movilidad ERASMUS
Parte A	  Parte B
HTML	indexParteA.html	indexParteB.html
Qué maquetas	Cabecera, menú y pie	Estructura de la página, cuadro de ayuda e interior del formulario
Técnica	Flexbox	Grid (cabecera, menú y pie siguen en Flexbox)


Comprobaciones de la Parte A

El CSS valida en jigsaw.w3.org/css-validator sin errores.
Usa flex-wrap, y al ampliar con Ctrl + + nada se corta.
La opción con aria-current va en negrita y con subrayado amarillo.
Los enlaces del menú se subrayan al pasar el ratón.

Entregable (GitHub)

Repositorio público diw-flexbox1-apellido-nombre.
Clonarlo y trabajar en esa carpeta.
Commits al terminar cada parte, con mensajes descriptivos.
README.md explicando el proceso seguido para estructurar la página.
Compartir la URL del repositorio en Moodle.


Todos lso pasos que he seguido para realizar la parte A

Paso 1. Preparar herramientas
Git: instálalo desde git-scm.com y compruebar en una terminal con git --version
VS Code: con la extensión Live Server para ver la página en el navegador y que se recargue sola
Cuenta de GitHub conectada a git del ordenador.
Configura tu identidad en Git una sola vez si no no tienes hecho ya de antes:

git config --global user.name "Carlos Plata Morán"
git config --global user.email "carplamor2506@iesfidiana.es"

Paso 2. Crear el repositorio en GitHub
En GitHub, en New repository.
Nombre: diw-flexbox1-plata-carlos.
En modo Public y Add a README file poque así el repositorio no está vacío al clonarlo.
Pulsa Create repository y copia la URL del repositorio en tu ordenador para conectarlos 

Paso 3. Clonar y organizar carpetas
En tu carpeta de trabajo subes todo el repositorio git que hemos creado para trabajar dentro de ese entorno 
git clone y la url de tu repositorio en el caso el mio 

Estructura 

diw-flexbox1-plata-carlos/
├── index.html        ← primero el contenido de indexParteA.html luego el de indexParteB.html
├── README.md
└── styles/
    └── estilos.css


Paso 4. CSS de la Parte A, bloque a bloque
Este es el HTML con el que trabajamos: header.cabecera (con .cabecera__marca y nav.menu), main.principal, footer.pie. Mira la Parte A: cabecera azul oscuro con la marca a la izquierda y el menú a la derecha, y el pie con el mismo azul, texto a la izquierda y enlaces a la derecha.
 Por tanto con estos colores predefinidos en el css arriba del todo hacemos un comentario con la paleta de colores a utilziar y una pequeña estructura para ver como queda todo y se ira actializando conforme añadamos cosas nuevas. 

4.2 Base

box-sizing: border-box evita sorpresas con paddings y anchos. El body en columna con min-height empuja el pie al fondo.
4.3 Cabecera y menú (Flexbox)
4.4 Contenido principal
4.5 Pie de página (Flexbox)

Paso 5. Comprobar la Parte A
En el navegador debe verse como la imagen con su cabecera con “Solicitud” en negrita y subrayada en amarillo, pie con enlaces subrayados.
Pasa el ratón por “Convocatoria” y comprueba que se subraya.
Recorre la página con el tabulador y comprueba que el foco se ve.
Haz Ctrl + + hasta el 200 % y estrecha la ventana: nada se corta y los elementos saltan de línea.
Valida el CSS en jigsaw.w3.org/css-validator .

Paso 6. Commit y push de la Parte A
git add .
git commit -m "Parte A: cabecera, menú y pie con Flexbox"
git push










GENERAL PARTE A + B TERMINADOS Y REDACTADOS:

# DAW Mobility · Solicitud de beca Erasmus+

Proyecto de la unidad 2 de Diseño de Interfaces Web (2.º DAW). Es una página con un formulario para solicitar una beca Erasmus+ de prácticas. Está dividido en dos partes que comparten el mismo repositorio:

- **Parte A:** cabecera, menú y pie de página con **Flexbox**.
- **Parte B:** estructura de la página, cuadro de ayuda e interior del formulario con **Grid**.

## Estructura del proyecto

```
diw-flexbox1-plata-moran-carlos/
├── indexParteA.html
├── indexParteB.html
├── README.md
└── styles/
    ├── estilosA.css
    └── estilosB.css
```

## Cómo preparé el entorno

1. Instalé Git y VS Code con la extensión Live Server para ver los cambios en el navegador al guardar.
2. Creé el repositorio público `diw-flexbox1-plata-moran-carlos` en GitHub con un README inicial.
3. Lo cloné en mi equipo con `git clone` y trabajé siempre dentro de esa carpeta.
4. Creé la carpeta `styles/` y enlacé la hoja de estilos desde el `<head>` de cada HTML.

## Parte A: Flexbox

Con el HTML ya dado y sus clases (siguen la metodología BEM), maqueté:

- **Cabecera:** `display: flex` con `justify-content: space-between` para dejar la marca a la izquierda y el menú a la derecha, y `flex-wrap: wrap` para que se reorganice en pantallas estrechas.
- **Menú:** lista en `flex`, sin viñetas. La opción con `aria-current="page"` va en negrita y con subrayado amarillo, y los enlaces se subrayan al pasar el ratón.
- **Pie:** el mismo planteamiento que la cabecera, con el texto a la izquierda y los enlaces a la derecha.
- **Cuerpo de la página:** `body` en columna con `min-height: 100vh` para que el pie quede siempre abajo.

## Parte B: Grid

### 1. Partir del nuevo HTML y de la misma hoja

Pasé a trabajar con `indexParteB.html`. La cabecera, el menú y el pie se quedan como estaban (Flexbox) y todo lo nuevo lo añadí a continuación en la misma hoja de estilos, en bloques con su comentario y actualizando el índice del principio.

### 2. Enfoque móvil primero

Decidí escribir por defecto lo que se ve en un móvil (todo en una columna) y usar solo dos consultas de medios con `min-width`:

- `40em`: para el interior del formulario.
- `56em`: para la estructura general de la página.

Todo lo demás se resuelve sin consultas de medios. Los tamaños y separaciones los puse en unidades relativas (`rem`, `em`, `%`), salvo los bordes finos.

### 3. Estructura general de la página

- `.principal` y `.contenido` pasan a ser grids de una columna.
- Usé `minmax(0, 1fr)` en lugar de `1fr` para que ningún hijo, como un campo de fecha o un `select`, pueda ensanchar la columna.
- El orden visual coincide con el orden del código: primero el formulario y debajo el cuadro de ayuda.
- En la consulta de `56em`, `.contenido` pasa a dos columnas (`minmax(0, 1fr) 18rem`) y el cuadro de ayuda se queda a la derecha con `position: sticky`.

### 4. Las tarjetas del formulario

Cada bloque del formulario (`.grupo`) tiene fondo blanco, borde fino, esquinas redondeadas y espacio interior. El título va sobre el borde, en azul oscuro y en negrita. Entre bloques dejé 1,5 rem de separación con el `gap` del formulario. Añadí `min-width: 0` a los `fieldset`, porque por defecto traen un ancho mínimo que provoca desbordes.

### 5. Los campos

Cada `.campo` es un grid de una columna, con el `gap` de 0,25 rem: la etiqueta arriba, el control debajo y la ayuda al final. Al principio las etiquetas salían al lado de los inputs, y lo resolví aplicando el grid al campo y no al contenedor del bloque. Los controles:

- ocupan todo el ancho del campo,
- miden como mínimo 44 px de alto,
- heredan la tipografía de la página (`font: inherit`),
- llevan un borde de 2 px con esquinas redondeadas.

La ayuda va a 0,875 veces el tamaño base y en el color de texto de ayuda de la paleta.

### 6. Rejilla de 6 columnas desde 40em

En la primera consulta de medios cada bloque pasa a una rejilla de 6 columnas iguales, con 1 rem entre filas y 1,5 rem entre columnas. Para colocar los campos usé `grid-template-areas` y `grid-area`, de forma que cada campo se coloca por su nombre y no por su posición en el código:

| Bloque | Fila 1 | Fila 2 | Fila 3 |
|---|---|---|---|
| Datos personales | Nombre (2) y Apellidos (4) | Correo (3) y Teléfono (3) | Fecha de nacimiento (2) |
| Datos académicos | Ciclo (3) y Curso (3) | Nota (2) e Idiomas (4) | |
| Preferencias de destino | País (3) e Incorporación (3) | Duración (6) | |
| Motivación y documentos | Carta (6) | Currículum (6) | |

### 7. Teléfono

El prefijo y el número van en la misma línea con un grid de dos columnas: la del prefijo mide entre 6 y 9,5 rem (`minmax(6rem, 9.5rem)`) para encogerse en pantallas estrechas y el número ocupa el espacio restante.

### 8. Opciones (radios y casillas)

- `.opciones__lista` usa `repeat(auto-fit, minmax(min(8rem, 100%), 1fr))`: reparte las opciones en tantas columnas como quepan, con al menos 8 rem, y se reorganiza solo, sin consultas de medios. El `min(8rem, 100%)` evita que la columna mínima sea mayor que el espacio disponible, ni siquiera con el texto ampliado al 200 %.
- Cada `.opcion` es un grid de dos columnas (casilla de 1,5 rem y texto), centrado en vertical y con 44 px de altura mínima.
- En la opción de privacidad el texto ocupa varias líneas, así que la casilla se alinea con la primera (`align-items: start`).

### 9. Pie de la carta y botonera

- En móvil, la ayuda de la carta y el límite de caracteres van uno debajo del otro. Desde `40em` pasan a la misma línea, la ayuda a la izquierda y el límite a la derecha.
- La botonera en móvil son tres botones apilados a todo el ancho. Desde `40em` es un grid con "Borrar formulario" a la izquierda, un hueco libre en medio y "Guardar borrador" y "Enviar solicitud" a la derecha.
- "Enviar" es el botón principal (fondo azul oscuro y texto blanco), "Guardar" tiene fondo blanco y borde azul y "Borrar" fondo blanco y borde gris. Todos miden al menos 44 px, con negrita y esquinas redondeadas.

### 10. Cuadro de ayuda

El cuadro de ayuda es una tarjeta con borde fino. Cada paso es un grid de dos columnas (`auto 1fr`): el número dentro de un círculo azul oscuro y el texto al lado, alineados arriba.

### 11. Accesibilidad

- Añadí estilos de foco visibles para el teclado (azul sobre fondo claro y amarillo sobre fondo oscuro). No quité el `outline`.
- El enlace "Saltar al contenido" queda escondido y aparece al llegar a él con el tabulador.
- Los campos inválidos se marcan con el borde en rojo.
- Usé los colores de la paleta indicada en el enunciado, cuyo contraste es suficiente.

## Problemas que tuve y cómo los resolví

- **Las etiquetas salían al lado de los inputs.** Aplicando `display: grid` a `.campo` quedaron apiladas.
- **Una media query de `768px` en `px`.** La sustituí por las dos de `40em` y `56em`, que son las únicas permitidas.
- **Colores fuera de la paleta.** Cambié los fondos de las tarjetas y del cuadro de ayuda al blanco de la paleta.
- **`git push` rechazado.** Había que traer primero el README que GitHub había creado con `git pull --no-rebase`, y luego repetir el push.

## Comprobaciones antes de entregar

- [ ] El CSS valida en jigsaw.w3.org/css-validator sin errores.
- [ ] Al ampliar el texto con Ctrl + + nada se corta.
- [ ] Se ve el foco al recorrer la página con el tabulador.
- [ ] En pantalla pequeña todo va en una columna, y a partir de 40em aparece la rejilla de 6 columnas.
- [ ] A partir de 56em el cuadro de ayuda queda a la derecha.
