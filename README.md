# Sandoval-L-pez
Temas escolares
Este es el html

 **
<DOCTYPE html >
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BrightTech</title>
</head>
<body>
  <header class="titulo">
    <h1>BrightTech</h1>
    <p>La mejor opción en Tecnología a tu disposición.</p>
  </header>
  <main>
    <section class="nosotros">
      <h2>Sobre Nosotros</h2>      
      <p>Somos la empresa de tecnología en la región con más y mejores productos, calidad y precio. 10 años de experiencia, avalada por millones de clientes y reseñas que respaldan la calidad de nuestros productos. .</p>
    </section>
    <section class="productos">
      <h2>Conoce Nuestros Productos</h2>
      <ul class="lista">
        <li>Impresoras 3D.</li>
        <li>Gafas de realidad.</li>
        <li>Asistentes Virtuales y Dispositivos de Hogar Inteligente.</li>
        <li>Dispositivos de hogar y Gaming.</li>
         <li>Cámaras Inteligentes de Seguridad.</li>
        <li>Drones y Equipos para Fotografía Aérea.</li>
        <li>Altavoces y Audífonos Inalámbricos.</li>
       
        <li>Software de Inteligencia Artificial.</li>
        <li>Y muchos más Accesorios para: Portátiles, Consolas y el Hogar. </li>
      </ul>
    </section>
  </main>
  <footer class="pie">
    <p>Todos los derechos reservados.</p>
    <p>Contacto: info@brighttech.com</p>
    <p>Alumno: Jesus Sandoval Lopez.</p>
  </footer>
</body>
</html>

**

// Variables
$background-color-body: #eee;
$font-family-body: arial, sans-serif;
$font-size-body: 16px;
$gradient-titulo-start: #155799;
$gradient-titulo-end: #159957;
$padding-standard: 1rem;
$text-color-light: #fff;
$box-shadow-productos: 0 4px 8px rgba(0, 0, 0, 0.9);
$border-radius-productos: 10px;
$max-width-productos: 600px;
$gradient-pie-start: #232526;
$gradient-pie-end: #414345;
$margin-top-pie: 4rem;

// Mixins
@mixin gradient-background($start-color, $end-color) {
  background: $end-color; // fallback for old browsers
  background: -webkit-linear-gradient(to right, $start-color, $end-color); // Chrome 10-25, Safari 5.1-6
  background: linear-gradient(to right, $start-color, $end-color); // W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+
}

@mixin box-style($padding, $bg-color, $box-shadow, $border-radius) {
  padding: $padding;
  background-color: $bg-color;
  box-shadow: $box-shadow;
  border-radius: $border-radius;
}

body {
  background-color: $background-color-body;
  font-family: $font-family-body;
  font-size: $font-size-body;
  margin: 0;
  padding: 0;
}

.titulo {
  @include gradient-background($gradient-titulo-start, $gradient-titulo-end);
  padding: $padding-standard;
  text-align: center;
  color: $text-color-light;
}

.nosotros {
  text-align: center;
  padding: $padding-standard;
}

.productos {
  @include box-style(20px, $background-color-body, $box-shadow-productos, $border-radius-productos);
  max-width: $max-width-productos;
  margin: 0 auto;
  text-align: center;
}

.lista {
  padding: 0;
  margin: 0 auto;
  display: inline-block;
  list-style: none;
}

.pie {
  @include gradient-background($gradient-pie-start, $gradient-pie-end);
  padding: 1px;
  color: $text-color-light;
  text-align: center;
  margin-top: $margin-top-pie;
}
