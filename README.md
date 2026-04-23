# MIXMEDIA
## Taller Multimedial
Semana 1 Ejercicio 1

```
<!DOCTYPE html>
<!-- Indica al navegador que este documento usa HTML5 -->

<html>
<!-- Inicio del documento HTML -->

<head>
<!-- Sección donde van metadatos, título y estilos -->

<meta charset="UTF-8">
<!-- Define la codificación de caracteres para que se vean bien tildes y símbolos -->

<title>Multimedial</title>
<!-- Título de la página que aparece en la pestaña del navegador -->

<style>
/* Aquí comienza la sección de estilos CSS que define la apariencia visual */

body{
/* "body" se refiere a todo el contenido visible de la página */

  background-color: #FFF1B5;
  /* Define que el fondo de toda la página sea blanco */

  color: black;
  /* Define que el color del texto sea negro */

  margin: 0;
  /* Elimina los márgenes que los navegadores agregan por defecto */

  height: 100vh;
  /* Hace que el alto del cuerpo sea igual al 100% de la altura de la pantalla */

  display: flex;
  /* Activa el sistema Flexbox para organizar y centrar elementos */

  justify-content: center;
  /* Centra el contenido horizontalmente */

  align-items: center;
  /* Centra el contenido verticalmente */

  font-family: Arial, sans-serif;
  /* Define la tipografía del texto */

  font-size: 60px;
  /* Define el tamaño grande del texto */

}
/* Fin de las reglas de estilo del body */

</style>
<!-- Fin de la sección de estilos -->

</head>
<!-- Fin de la sección head -->

<body>
<!-- Inicio del contenido visible de la página -->

MIXMEDIA
<!-- Texto que aparece en el centro de la pantalla -->

</body>
<!-- Fin del contenido visible -->

</html>
<!-- Fin del documento HTML -->
```

DECLARACION DE IA
```

CÓDIGO OBRAS.HTML ANTIGUO

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Obras</title>

    <style>
        /* Estilo general del cuerpo */
        body {
            background-color:brown;
            font-family: Arial, sans-serif;
            margin: 0;

        }
.abajo {
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    background-color: brown;
    padding: 10px;
    width: 100%;
}


        /* Sección o bloque */
        .bloque {
            background-color: white;
            margin: 15px 0;
            width: 400px;
            padding: 25px;
            text-align: center;
            box-sizing: border-box;
            transition: 0.5s;
            overflow: hidden;
        }


         /* Encabezado */
        .bloque h2 {
            margin-top: 20px;
        }

        /* Imagen */
        .bloque img {
            width: 95%;
            height: auto;
            transition: transform 0.5s ease;
        }

        .bloque:hover img {
        transform: scale(1.1);
        }

        .bloque:hover .overlay {
        opacity: 1;
        }


        /* Texto */
        .bloque p {
            line-height: 1.5;
        }



        .boton { /* Define una clase llamada "boton" */
         background-color: rgb(104, 8, 24); /* Color de fondo del botón */
         color: white; /* Color del texto */
         padding: 25px; /* Espacio interno (arriba, abajo, izquierda, derecha) */
         width: 150px; /* Ancho fijo del botón */
         text-align: center; /* Centra el texto horizontalmente */
         transition: 0.3s; /* Hace que los cambios (como color) sean suaves en 0.3 segundos */
        }

        .boton:hover { /* Se activa cuando el mouse pasa sobre el elemento */
         background-color: rgb(170, 85, 85); /* Cambia el color de fondo al pasar el mouse */
        }

        
    </style>
</head>

<body>


    <!-- Contenedor principal -->

<a href="index.html" class="boton">Volver</a>

<h1 style="text-align:center;">Obras</h1>

<div class="abajo">
<div class="bloque">
    <img src="img/alucinaciondeconsuelo.jpg" alt="Alucinación de consuelo">
    <h3>2025</h3>
    <p>Impresiones sobre papel</p>
</div>
    <div class="bloque">
    <img src="img/amalgama.jpg" alt="Amalgama">
    <h3>2025</h3>
    <p>Tecnica mixta </p>
</div>
</div>
<div class="abajo">
    <div class="bloque">
    <img src="img/ornamentacionquiensabe.jpg" alt="ornamentacionquiensabe">
    <h4>2026</h4>
    <p>Impresiones sobre papel </p>
</div>
   <div class="bloque">
<img src="img/serigrafia.jpg" alt="seri">
    <h4>2025</h4>
    <p> Serigrafia sobre papel </p>
 </div>
 </div>



</body>
</html>
```

CÓDIGO GEMINI

```
necesito ordenar imágenes en la pagina web, donde esten en un grupo de 4 del mismo tamaño y que cuando el mouse pase por encima de las imágenes se pueda apreciar el nombre y año de la obra


código entregado por gemini

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Obras</title>
    <style>
        body {
            background-color: brown;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }

        /* Contenedor principal: Grid de 4 columnas */
        .contenedor-obras {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Cada bloque de imagen */
        .bloque {
            position: relative; /* Necesario para posicionar el texto encima */
            aspect-ratio: 1 / 1; /* Mantiene las imágenes cuadradas y del mismo tamaño */
            overflow: hidden;
            background-color: #000;
            border-radius: 8px;
        }

        /* Imagen que ocupa todo el bloque */
        .bloque img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Recorta la imagen para que llene el cuadrado sin deformarse */
            transition: transform 0.5s ease;
            display: block;
        }

        /* Capa oscura con el texto (oculta por defecto) */
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7); /* Fondo negro semitransparente */
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0; /* Invisible */
            transition: opacity 0.4s ease;
            text-align: center;
            padding: 10px;
            box-sizing: border-box;
        }

        /* Efectos al pasar el mouse */
        .bloque:hover img {
            transform: scale(1.1);
        }

        .bloque:hover .overlay {
            opacity: 1; /* Muestra el texto */
        }

        .overlay h3 { margin: 0; font-size: 1.2rem; }
        .overlay p { margin: 5px 0 0; font-size: 0.9rem; }

        /* Botón Volver */
        .boton {
            display: inline-block;
            background-color: rgb(104, 8, 24);
            color: white;
            padding: 15px 25px;
            text-decoration: none;
            margin-bottom: 20px;
            transition: 0.3s;
        }

        .boton:hover {
            background-color: rgb(170, 85, 85);
        }

        h1 { color: white; margin-bottom: 30px; }
    </style>
</head>
<body>

    <a href="index.html" class="boton">Volver</a>
    <h1 style="text-align:center;">Obras</h1>

    <div class="contenedor-obras">
        <div class="bloque">
            <img src="img/alucinaciondeconsuelo.jpg" alt="Alucinación de consuelo">
            <div class="overlay">
                <h3>Alucinación de Consuelo</h3>
                <p>2025 - Impresiones sobre papel</p>
            </div>
        </div>

        <div class="bloque">
            <img src="img/amalgama.jpg" alt="Amalgama">
            <div class="overlay">
                <h3>Amalgama</h3>
                <p>2025 - Técnica mixta</p>
            </div>
        </div>

        <div class="bloque">
            <img src="img/ornamentacionquiensabe.jpg" alt="Ornamentación">
            <div class="overlay">
                <h3>Ornamentación</h3>
                <p>2026 - Impresiones sobre papel</p>
            </div>
        </div>

        <div class="bloque">
            <img src="img/serigrafia.jpg" alt="Serigrafía">
            <div class="overlay">
                <h3>Serigrafía</h3>
                <p>2025 - Serigrafía sobre papel</p>
            </div>
        </div>
    </div>

</body>
</html>

CODIGO INDEX ANTIGUO

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<!-- Define la codificación de caracteres para que se vean bien tildes y símbolos -->
<title>Multimedial</title>


    <style>
        /* Estilo general del cuerpo */
        body {
            background-image: url(img/fondo.jpg);
            font-family: Arial, sans-serif;
            margin: 0;
            display: flex; /* Activa flexbox */
            justify-content: center; /* Centra horizontalmente */
            align-items: center; /* Centra verticalmente */
            height: 100vh; /* Altura total de la pantalla (viewport height) */
        }

        /* Contenedor principal */
        .contenedor {
            width: 20%;
            margin: auto;
        }

        /* Sección o bloque */
        .bloque {
            background-color: rgba(255, 255, 255, 0.474);
            margin: 20px 0;
            padding: 50px;
            width: 300px;
            justify-content: center; /* Centra horizontalmente */
            align-items: center; /* Centra verticalmente */
            transition: 0.3s; /* Hace que los cambios (como color) sean suaves en 0.3 segundos */
            
        }

        .bloque:hover{
        background-color: white;
        padding: 70px;

        }


        /* Sección o bloque */
        .bloque h2{
           margin-top: 10px;
        }

        nav a {
            margin-left: 20px;
            text-decoration: none;
            color:black;
            font-size: 20px;
            transition: 0.3s;

        }

        nav a:hover {
            font-size: 30px;
        }

</style>
<!-- Fin de la sección de estilos -->



</head>
<!-- Fin de la sección head -->

<body>
    <div class="contenedor">
        <div class="bloque">
            <h1>Antonia Castro</h1>
<nav>
<a href="obras.html">Obras</a><br>
<a href="contacto.html">Contacto</a>
</nav>
        </div>
    </div>
</body>
<!-- Fin del contenido visible -->

</html>
<!-- Fin del documento HTML →



CÓDIGO GEMINI

necesito ordenar imágenes en la página web, donde esten en un grupo de 4 del mismo tamaño y que cuando el mouse pase por encima de las imágenes se pueda apreciar el nombre y año de la obra


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Multimedial</title>
    <style>
        body {
            background-image: url('img/fondo.jpg');
            background-size: cover;
            background-position: center;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
        }

        .bloque {
            background-color: white; /* Blanco sólido */
            padding: 40px 60px;      /* Espacio inicial */
            display: inline-block;   /* El ancho lo define el contenido */
            text-align: center;
            transition: all 0.4s ease; /* Esta es la animación que quieres */
            cursor: default;
            box-shadow: 0px 10px 25px rgba(0,0,0,0.1);
        }

        /* La animación que expande el bloque blanco */
        .bloque:hover {
            padding: 70px 90px;      /* Aumenta el tamaño hacia afuera */
            box-shadow: 0px 15px 35px rgba(0,0,0,0.2);
        }

        h1 {
            margin: 0;
            font-size: 30px;
            color: black;
            /* Evita que el nombre se mueva a dos líneas */
            white-space: nowrap; 
        }

        nav {
            margin-top: 20px;
        }

        nav a {
            display: block;
            text-decoration: none;
            color: black;
            font-size: 20px;
            margin: 10px 0;
            transition: 0.3s;
        }

        nav a:hover {
            font-size: 30px; /* Tu animación de los enlaces */
        }
    </style>
</head>
<body>

    <div class="bloque">
        <h1>Antonia Castro</h1>
        <nav>
            <a href="obras.html">Obras</a>
            <a href="contacto.html">Contacto</a>
        </nav>
    </div>

</body>
</html>

CÓDIGO ANTIGUO CONTACTO

quiero editar esta pagina <!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Obras</title>

    <style>
        /* Estilo general del cuerpo */
        body {
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            background-color: #fff2cd;
            margin: 0;
        }

        /* Contenedor principal */
        .contenedor {
            width: 60%;
            margin: auto;
        }

        /* Sección o bloque */
        .bloque {
            background-color: white;
            margin: 20px 0;
            padding: 50px;
            border-radius: 10px;
        }

        /* Imagen */
        .bloque img {
            width: 30%;
            height: auto;
        }

        /* Encabezado */
        .bloque h2 {
            margin-top: 20px;
        }

        /* Texto */
        .bloque p {
            line-height: 1.5;
        }

        .boton { /* Define una clase llamada "boton" */
         background-color: rgb(104, 8, 24); /* Color de fondo del botón */
         color: white; /* Color del texto */
         padding: 15px; /* Espacio interno (arriba, abajo, izquierda, derecha) */
         width: 150px; /* Ancho fijo del botón */
         text-align: center; /* Centra el texto horizontalmente */
         transition: 0.3s; /* Hace que los cambios (como color) sean suaves en 0.3 segundos */
        }

        .boton:hover { /* Se activa cuando el mouse pasa sobre el elemento */
         background-color: rgb(170, 85, 85); /* Cambia el color de fondo al pasar el mouse */
        }


        
    </style>
</head>

<body>

<!-- BLOQUE 4 -->
        <div class="bloque">
            <h2>Contacto</h2>
            <img src="img/mmmgatete.jpg" alt="Imagen de contacto">
            <h3>acastroc2@uft.edu</h3>
            <h4>@missupyon</h4>
        </div>

</div>

        <a href="index.html" class="boton">Volver</a>

        </div>
</body>
</html>

CÓDIGO NUEVO CONTACTO

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Contacto</title>

    <style>
        /* Estilo general del cuerpo */
        body {
            /* Usé el color brown para ser consistente con "Obras", 
               pero puedes cambiarlo a #fff2cd si prefieres el crema */
            background-color: brown; 
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            margin: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* Bloque central de contacto */
        .bloque-contacto {
            background-color: white;
            padding: 50px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0px 10px 30px rgba(0,0,0,0.2);
            width: 100%;
            max-width: 400px; /* Tamaño similar al index */
            transition: transform 0.3s ease;
        }

        .bloque-contacto:hover {
            transform: scale(1.02);
        }

        /* Imagen de contacto circular */
        .bloque-contacto img {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 50%; /* Hace la imagen circular */
            margin-bottom: 20px;
            border: 5px solid #f0f0f0;
        }

        .bloque-contacto h2 {
            margin: 10px 0;
            color: #333;
            font-size: 28px;
        }

        .bloque-contacto h3 {
            color: rgb(104, 8, 24);
            font-size: 18px;
            margin: 5px 0;
        }

        .bloque-contacto h4 {
            color: #666;
            font-weight: normal;
            margin-bottom: 20px;
        }

        /* Botón Volver */
        .boton {
            display: inline-block;
            background-color: rgb(104, 8, 24);
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            text-align: center;
            transition: 0.3s;
            margin-top: 30px;
            border-radius: 5px;
        }

        .boton:hover {
            background-color: rgb(170, 85, 85);
        }
        
    </style>
</head>

<body>

    <div class="bloque-contacto">
        <img src="img/mmmgatete.jpg" alt="Imagen de contacto">
        <h2>Contacto</h2>
        <h3>acastroc2@uft.edu</h3>
        <h4>@missupyon</h4>
    </div>

    <a href="index.html" class="boton">Volver al Inicio</a>

</body>
</html>

/* Quita el subrayado y mantiene los colores que ya elegiste */
.link-contacto {
    text-decoration: none;
    transition: 0.3s;
    display: inline-block;
}

/* Efecto visual cuando el usuario pasa el mouse sobre el correo o el IG */
.link-contacto:hover {
    opacity: 0.7;
    transform: translateY(-2px); /* Pequeño salto hacia arriba */
}

/* Asegura que los encabezados dentro del link no cambien de color */
.link-contacto h3, .link-contacto h4 {
    margin: 5px 0;
}
```
