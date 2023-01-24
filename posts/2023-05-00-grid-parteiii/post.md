# Placa 1 - Introducción
Hoy en coopademia: CSS Grid Parte III: grid áreas

# Placa 2 -
Decidimos dejarle una caoopedemia especial para gird areas, porque con esta herramienta es posible indicar el nombre y la posición concreta de cada área de la cuadrícula. Utiliza la propiedad grid-template-areas, donde debes especificar el orden de las áreas. Luego, en cada ítem hijo, usas la propiedad grid-area para indicar el nombre del área en cuestión.



# Placa 3 -Veamos un poco de código - Este sería el HTMLl 

```
<div id="grilla">
 	<header class="border">Header</header>
 	<section id="productos" class="border">Section</section>
 	<section id="servicios" class="border">Section</section>
 	<nav class="border">Navegacion</nav>
 	<aside class="border">Aside</aside>
 	<footer class="border">Pie de pagina</footer>
</div>

```

# Placa 4 - Veamos un poco de código - Este sería el css

#grilla {
   display: grid;
   grid-template-areas:
     "nav header header"
     "nav productos publicidad"
     "nav servicios publicidad"
     "nav footer footer";
   grid-template-rows: 100px 1fr 1fr 75px; 
   grid-template-columns: 20% auto 15%;
}
.border {
   border: 1px solid black;
}

header {
   grid-area: header;
}
footer {
   grid-area: footer;
}
section#productos {
   grid-area: productos;     
}
section#servicios {
   grid-area: servicios;     
}
nav {
   grid-area: nav;
}
aside {
   grid-area: publicidad;
}


# Placa 5 - ¿Cuáles son las ventajas? 
De esta forma tendríamos una estructura bidimensional que luego podemos cambiar fácilmente y adaptarla con los media queries para diferentes tamaños de pantalla, con una grilla mucho más visual en nuestro código. Podés probar el ejemplo en tu editor de código.

# Placa 7 - Imagen final con el logo de Devecoop.

¡Hasta la próxima!
