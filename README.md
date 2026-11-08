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
