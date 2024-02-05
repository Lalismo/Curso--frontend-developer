# Curso--frontend-developer

## ¿Qué son y para qué nos sirve HTML & CSS ?

HTML es un lenguaje de hipertexto que sirve para estructurar toda nuestra base de la pagina web.
CSS es una hoja de estilos en cascada y es el lenguaje que le da "vida" a nuestro esqueleto de HTML
en el se pueden hacer diferentes cosas como colores, tamaño, ubicaciones y más..

## Motores de renderizado

Lo que hace los motores es hacer que los navegadores puedan mostrar lo que nosotros escribirmos del HTML Y CSS
en una pagina web

Algunos navegadores con su motor:

```
Chrome  ->  Blink
Edge    ->  Edge HTML
Safari  ->  Wenkit
Firefox -> Gecko
```

> [!IMPORTANT]
> El navegador hace 5 pasos

1. Pasa los archivos a objetos.
2. calcula el estilo correspondiente a cada nodo Dom.
3. Calcula las dimensiones de cada nodo y dónde va en la pantalla.
4. Pinta las diferentes cajas.
5. Las convierte en una imagen para mostrar en pantalla.


## Anatomia de un documento HTML y sus elementos

Elemento:
```
<h1>   -> Etiqueta de apertura
Platzi -> Contenido
</h1>  -> Etiqueta de cierre
```
Atributo:
```
<h1 class = "title">

    |           |
    v           v
Atributo      Valor  
```

### Anidamiento
Es colocar las cosas conforme se van utilizando, el anidamiento ayuda a tener un mejor orden en nuestro codigo,
haciendo que sea más legible y entendible.
<section>
    <h1> Platzi </h1>
    <p> Tiene una comunidad </p>
    <ul>
        <li>Increíble</li>
        <li>Maravilloso</li>
    </ul>
</section>

### Elementos vacíos
Hay etiquetas en hmtl que no necesita necesariamente un cierre en el caso de img no tiene, ya que el url de la imagen 
se encuentra dentro de la etiqueta.
<img src="cat.jpg" alt="cat">

### Estructura principal de HTML

<!DOCTYPE html> --> Es un indicador para enseñar que se esta trabajando con un archivo HTML
<html lang="en">--> Es la etiqueta más importante, ya qué dentro esta contiene toda la estructura HTML y es donde se asigna el idioma en que se escribe el codigo
<head> --> Es la cabecera de nuesta pagina y podremos encontrar como los iconos de empresas, titulos, links, etc
    <meta charset="UTF-8">
    <title> Mi portafolio </title>
</head>
<body>--> Es donde se contiene toda la estructura de nuestro HTML y de nuestra pagina web
    <header>
    <nav>
    <section>
    <footer>
</body>
</html>

## ¿QUÉ ES HTML SEMÁNTICO?

Es una ayuda para hacer que nuestro HTML sea legible y este ordenado, también el solo hacer uso de div no es buena idea
Lo mejor es hacerlo por secciones cada una con sus respectivas etiquetas como lo es header, ul, footer, etc.

### Ejemplo en codigo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <header> Hola </header>
    <nav>
        <ul></ul>
    </nav>
</body>
</html>

## Etiquetas HTML Más utilizadas


```   
Layout          Textos          Formularios     Enlaces     Imagenes & videos       Listas                  
* HEADER        * h1 ... h6     * Form          * a         * img                   * ul
* NAV           * P             * Input                     * svg                   * li
* SECTION                       * Label                     * iframe                * ol
* ARTICLE                       * Button                    * video
* FOOTER
```

## Anatomía de una declaración CSS: selectores, propiedades y valores

Selector
^      Propiedad 
|      ^ 
h1 {   | 
    color: pink; -> Valor
}

## Tipos de selectores: básicos y combinados

Selectores básicos
```
De tipo     -> div {...}

De clase    -> .elemento {...}

De id       -> #id(del elemento){...}

De atributo -> a[href="..."] {...}

Universal   -> *{...}
```
### Ejemplo en codigo

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    * {
      background: papayawhip;
    }
    div {
      background: pink;
    }
    .titulo {
      color: blueviolet;
    }
    #titulo2 {
      color: brown;
    }
    a[href="https://platzi.com/home"] {
      color: blue;
    }
  </style>
</head>
<body>
  <div class="titulo">Hola</div>
  <div id="titulo2">mundo</div>
  <a href="https://platzi.com/home">Platzi</a>
</body>
</html>

Selectores combinados
```
Descendientes       -> div p

Hijo directo        -> div > p

Elemento adyacente  -> div + p

General de hermanos -> div ~ p
```

### Ejemplo en codigo

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    div p {
      color: Lime;
    }
    div > div {
      background: plum;
    }
    .es {
      background: red;
    }
    div + section {
      background: palevioletred;
    }
    div ~ p {
      color: powderblue;
    }
  </style>
</head>
<body>
  <div>
    <div>
      <p>Platzi</p>
      <div class="es">Es</div>
    </div>
  </div>
  <p>Clase de selectores</p>
  <p>Clase de selectores</p>
  <section>
    Es lo mejor
  </section>
  <div>
    Master
  </div>
</body>
</html>

## Tipos de selectores: pseudoclases y pseudoelementos

Pseudoclases: llegar a ciertas acciones que hace el usuario como por ejemplo al hacer clic al botón

Pseudoelemento: Son aquellos que nos permiten acceder a elementos de html que no son accesibles con algunos tipos de selectores como ejemplo la primera letra de un texto o si se quiere agregar contenido antes o despues de un texto

```
Pseudoclases        Pseudoelementos

* :active            * ::after
* :focus             * ::before
* :hover             * ::first-letter
* :nth-child(n)      * ::placeholder
```

## Cascada y especifidad en CSS

```
C - Cascading
S - Style
S - Sheet
```
Cascada -> Significa que el orden de las reglas en css **importa**

Ejemplo
<h1>

h1 {
    color: red;
}

h1 {
    color: blue;
}
La etiqueta <h1> tendrá un color blue de letra, esto porque está situado más abajo en el código. Esto ocurre con cada propiedad de CSS que se repita en algún punto más arriba del código.

### Qué es especificidad en CSS

La especificidad consiste en dar un valor a una recla CSS sobre **qué tan especifico es el estilo**, esto para que los navegadores puedan ssaber qué estilos aplicar sobre otros,
independientemente de dónde se encuentren en el código. **El estilo se aplicará donde la especifidad sea mayor**

### Tipos de especifidad en CSS

Existen 6 tipos de especifidad con su respectivo valor, donde X es la cantidad de estilos que lo contienen.

¿Cómo podemos saber qué reglas de CSS tienen mayor especificidad?
```
X o o o o | !important
  X o o o | Estilos en línea
    X o o | #ID
      X o | Clases, atributos y pseudoclases
        X | Elementos y pseudoelementos
        o | Selector universal
```

### Regla con mayor especificidad

La palabra reservada **!important** Es **un valor de toda propiedad CSS que provee una especificidad de 10000**, por lo que se aplicará ante otros estilos.

##Tipos de display más utilizados: block, inline e inline-block

Display: es el tipo de vizualización que tendran los elementos html en nuestra pagina

### Visualización en bloque (block)

El display **block** establece que un elemento ocupará todo el espacio disponible por defecto y el siguiente elemento a este se situará por debajo.
Es posible añadir medidas de anchura **width** y algura **height** a estos elementos.

También esposible agregar todas las propiedades del modelo de caja.

En este sitio podrás encontrar un ejemplo [Ejemplo block](https://codi.link/PGRpdj5Tb3kgZGlzcGxheSBibG9jazwvZGl2Pg0KPGRpdj5Tb3kgZGlzcGxheSBibG9jazwvZGl2Pg0KPGRpdiBjbGFzcz0iY29uX21lZGlkYXMiPlNveSBkaXNwbGF5IGJsb2NrPC9kaXY+DQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KZGl2ew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KICAvKiBtYXJnaW46IDEwcHg7ICovDQogIC8qIHBhZGRpbmc6IDEwcHg7ICovDQp9DQoNCi5jb25fbWVkaWRhcyB7DQogIC8qIHdpZHRoOiAyMDBweDsgKi8NCiAgLyogaGVpZ2h0OiAyMDBweDsgKi8NCn0NCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4ycmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCg0KDQo=%7C).

### Visualización en línea (inline)

El display **inline** establcec que un elemento ocupará el espacio del contenido del mismo y el siguiente elemento se situará a la derecha.
**No es posible añadir medidas de anchura **width** y altura **height** a estos elementos.**

También, no es posible agregar todas las propiedades del modelo de caja, únicamente funcionará la propiedad margin en el eje horizontal.

En este sitio podrás encontrar un ejemplo [Ejemplo inline](https://codi.link/PGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24+U295IGRpc3BsYXkgaW5saW5lLWJsb2NrPC9idXR0b24+DQo8YnV0dG9uPlNveSBkaXNwbGF5IGlubGluZS1ibG9jazwvYnV0dG9uPg0KPGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24gY2xhc3M9ImNvbl9tZWRpZGFzIj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCg0K%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KYnV0dG9uew0KICAvKiBtYXJnaW46IDEwcHg7ICovDQogIC8qIHBhZGRpbmc6IDEwcHg7ICovDQp9DQoNCi5jb25fbWVkaWRhcyB7DQogIC8qIHdpZHRoOiAzMDBweDsgKi8NCiAgLyogaGVpZ2h0OiAxMDBweDsgKi8NCn0NCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4xcmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCg0KDQo=%7C).

### Visualización de bloque y linea (inline-block)

El display **inline-block** combina las ventajas de block para colocar medidas al elemento y propiedades del modelo de caja correctamente; con las ventajas de inline de color para un elemento seguido de otro en el mismo espacio.

Si el elemento excede el contenido total, se coloca en la siguiente línea por debajo.

En este sitio podrás encontrar un ejemplo [Ejemplo inline-block](https://codi.link/PGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24+U295IGRpc3BsYXkgaW5saW5lLWJsb2NrPC9idXR0b24+DQo8YnV0dG9uPlNveSBkaXNwbGF5IGlubGluZS1ibG9jazwvYnV0dG9uPg0KPGJ1dHRvbj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCjxidXR0b24gY2xhc3M9ImNvbl9tZWRpZGFzIj5Tb3kgZGlzcGxheSBpbmxpbmUtYmxvY2s8L2J1dHRvbj4NCg0K%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KYnV0dG9uew0KICAvKiBtYXJnaW46IDEwcHg7ICovDQogIC8qIHBhZGRpbmc6IDEwcHg7ICovDQp9DQoNCi5jb25fbWVkaWRhcyB7DQogIC8qIHdpZHRoOiAzMDBweDsgKi8NCiAgLyogaGVpZ2h0OiAxMDBweDsgKi8NCn0NCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4xcmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCg0KDQo=%7C).


## Tipos de display ,ás usados: flexbox y CSS grid

El display flex y grid son formas de visualización de elementos recientes y cada uno tiene sus propias características para crear interfaces de manera efectiva, a partir de un contenedor padre que dotará a los elementos hijos de superpoderes del posicionamiento.

Ambas herramientas tienen temas muy extensos de entender, y como intención no es estresarte con demasiada información, simplemente ten presente de namera general en qué consisten.

### Qué es flexbox

Flexbox consiste en el ordenamiento de elementos hijos en un solo eje, por defecto horizontalmente. El elemento padre o contenedor deberpa contener la propiedad display con el valor flex. A partir de aquí, ya puedes ordenar los hijos según sea necesario.

En este sitio podrás encontrar un ejemplo [Ejemplo flexbox](https://codi.link/PGRpdiBjbGFzcz0iY29udGFpbmVyIj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCjwvZGl2Pg0KDQoNCg0K%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCiAgYm94LXNpemluZzogYm9yZGVyLWJveDsNCn0NCg0KLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KLmNvbnRhaW5lcnsNCiAgLyogZGlzcGxheTogZmxleDsgKi8NCn0NCg0KLmNvbnRhaW5lciBkaXYgew0KICB3aWR0aDogMTAwcHg7IA0KICBoZWlnaHQ6IDEwMHB4Ow0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4pew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4rMSl7DQogIGJhY2tncm91bmQtY29sb3I6IGJyb3duOw0KfQ0KDQoNCg0KDQoNCg0K%7C).

Acá esta una guía completa para Flexbox [Guía flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

### Que es grid

Grid consiste en el ordenamiento de elementos hijos en dos ejejs, como si fuera una cruadrícula o tabla. El elemento padre o contenedor deberpa contener la propiedad dosplay con el valor grid y debes definir las medidas de las columnas y de las filas. A partir de aquí, ya puedes ordenar los hijos según sea necesario.

En este sitio podrás encontrar un ejemplo [Ejemplo grid](https://codi.link/PGRpdiBjbGFzcz0iY29udGFpbmVyIj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCiAgPGRpdj48L2Rpdj4NCjwvZGl2Pg0KDQoNCg0K%7CKiB7DQogIG1hcmdpbjogMDsNCiAgcGFkZGluZzogMDsNCiAgYm94LXNpemluZzogYm9yZGVyLWJveDsNCn0NCg0KLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KLmNvbnRhaW5lcnsNCi8qICAgDQogIGRpc3BsYXk6IGdyaWQ7DQogIGdyaWQtdGVtcGxhdGUtY29sdW1uczogMTAwcHggMTAwcHggMTAwcHg7DQogIGdyaWQtdGVtcGxhdGUtcm93czogMTAwcHggMTAwcHggMTAwcHg7IA0KICAqLw0KDQoNCn0NCg0KLmNvbnRhaW5lciBkaXYgew0KICB3aWR0aDogMTAwcHg7IA0KICBoZWlnaHQ6IDEwMHB4Ow0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4pew0KICBiYWNrZ3JvdW5kLWNvbG9yOiBhcXVhOw0KfQ0KDQouY29udGFpbmVyIGRpdjpudGgtY2hpbGQoMm4rMSl7DQogIGJhY2tncm91bmQtY29sb3I6IGJyb3duOw0KfQ0KDQoNCg0KDQoNCg0K%7C).

Acá esta una guía completa para Grid [Guía grid](https://css-tricks.com/snippets/css/complete-guide-grid/).

## Modelo de caja

El modelo de caja se compone de cuatro elementos: margin, border, padding y contenido

### Contenido del elemeneto HTML

El contenido del elemento, como su nombre lo indica, es todo lo que está dentro del elemento. Este tiene medidas establecidas por las propiedades width y height, que representa la anchura y la altura, respectivamente, Si imaginamos una caja, este valor sería todo lo que decidas colocar dentro.

```
div{
  width: 100px;
  height: 100px;
}
```

### Espaciado interno del elemento HTML o padding

El padding consiste en el espacio entre el borde y el contenido del elemento HTML. Si imaginamos una caja, este valor sería el espacio entre la caja y lo que guardes dentro.

```
div{
  padding: 100px;
}
```

En este sitio podrás encontrar un ejemplo [Ejemplo padding](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBlbCBjb21wb3J0YW1pZW50byAqLw0KZGl2ew0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQogIGJhY2tncm91bmQtY29sb3I6IGdyZWVueWVsbG93Ow0KICBib3JkZXI6IHNvbGlkIDFweCBibGFjazsNCiAgLyogcGFkZGluZzogMzBweDsgKi8NCn0NCg0KDQoNCi8qIElnbm9yYSBlc3RvcyBlc3RpbG9zLCBwb3IgYWhvcmEgKi8NCiogew0KICBmb250LXNpemU6IDEuMXJlbTsNCiAgbWFyZ2luOiAwLjVyZW07DQp9DQo=%7C)

También se puede establecer el padding en cada posición en una sola línea de las siguientes maneras:

```
padding: [arriba][derecha][abajo][izquierda], siguiendo el sentido horario.
padding: [arriba][derecha e izquierda][abajo], siguiendo el eje principal.
padding: [arriba y abajo] [derecha e izquierda], siguiendo el eje del elemento.
```

También estableciendo de manera individual los valores de cada posición:
```
div {
    padding-top: 10px;
    padding-bottom: 15px;
    padding-left: 20px;
    padding-right: 10px;
}
```

### Bordes del elemento HTML

El border consiste en el perfil o borde de un elemento HTML. Si imaginamos una caja, sería la caja en sí. Para definir un borde es necesario utilizar las siguientes tres propiedades:

```
border-color: establece el color del borde.
border-style: establece el estilo propio del borde, estos pueden ser: none (sin borde), dotted (puntos), dashed (guiones), solid (continuo), double (doble continuo), groove (recuadro).
border-width: estable la anchura del borde.
```

También se puede establecer los tres valores en una sola propiedad border donde no importa el orden.

```
div {
    border: [color] [style] [width];
}

div {
    border-color: red;
    border-style: solid;
    border-width: 1px;
}
```

También estableciendo de manera individual los valores de cada posición:

```
div {
  border-top: 5px solid blue;
  border-bottom: 5px solid red;
  border-left: 5px solid black;
  border-right: 5px solid yellow;
}
```

En este sitio podrás encontrar un ejemplo [Ejemplo border](https://codi.link/PGRpdiBjbGFzcz0ibm9uZSI+U2luIGJvcmRlPC9kaXY+DQo8ZGl2IGNsYXNzPSJkb3R0ZWQiPkNvbiBwdW50b3M8L2Rpdj4NCjxkaXYgY2xhc3M9ImRhc2hlZCI+Q29uIGd1aW9uZXM8L2Rpdj4NCjxkaXYgY2xhc3M9InNvbGlkIj5Db250aW51bzwvZGl2Pg0KPGRpdiBjbGFzcz0iZG91YmxlIj5kb2JsZSBjb250aW51bzwvZGl2Pg0KPGRpdiBjbGFzcz0iZ3Jvb3ZlIj5Db24gcmVjdWFkcm88L2Rpdj4NCg0KDQo=%7CZGl2ew0KICB3aWR0aDogMTIwcHg7DQogIGhlaWdodDogMTIwcHg7DQp9DQoNCi5ub25lew0KICAvKiBWYWxvciBwb3IgZGVmZWN0byBkZSBkaXYgKi8NCiAgYm9yZGVyOiAzcHggYmxhY2sgbm9uZTsNCn0NCg0KLmRvdHRlZHsNCiAgYm9yZGVyOiAzcHggYmxhY2sgZG90dGVkOw0KfQ0KDQouZGFzaGVkew0KICBib3JkZXI6IDNweCBibGFjayBkYXNoZWQ7DQp9DQoNCi5zb2xpZHsNCiAgYm9yZGVyOiAzcHggYmxhY2sgc29saWQ7DQp9DQoNCi5kb3VibGV7DQogIGJvcmRlcjogM3B4IGJsYWNrIGRvdWJsZTsNCn0NCg0KLmdyb292ZXsNCiAgYm9yZGVyOiA1cHggZ3JlZW55ZWxsb3cgZ3Jvb3ZlOw0KfQ0KDQoNCg0KLyogSWdub3JhIGVzdG9zIGVzdGlsb3MsIHBvciBhaG9yYSAqLw0KKiB7DQogIGZvbnQtc2l6ZTogMS4xcmVtOw0KICBtYXJnaW46IDA7DQp9DQoNCmJvZHl7DQogIGRpc3BsYXk6IGZsZXg7DQogIGZsZXgtd3JhcDogd3JhcDsNCiAgZ2FwOiAxLjVyZW07DQogIG1hcmdpbjogMjBweDsNCiAgZm9udC13ZWlnaHQ6IDgwMDsNCn0NCg0KDQoNCg==%7C).

### Espaciado externo del elemento HTML o margin

El margin consiste en el espacio entre el borde y otro elemento HTML. Si imaginamos una caja, es el espacio entre tu caja y otra caja.

```
div {
    margin: 10px;
}
```

Puedes establecer el margin en cada posición en una sola línea de las siguientes maneras:
```
margin: [arriba] [derecha] [abajo] [izquierda], siguiendo el sentido horario.
margin: [arriba] [abajo] [derecha e izquierda], siguiendo el eje principal.
margin: [arriba y abajo] [derecha e izquierda], siguiendo los ejes del elemento.
```

También estableciendo de manera individual los valores de cada posición:
```
margin: [arriba] [derecha] [abajo] [izquierda], siguiendo el sentido horario.
margin: [arriba] [abajo] [derecha e izquierda], siguiendo el eje principal.
margin: [arriba y abajo] [derecha e izquierda], siguiendo los ejes del elemento.
```

### Valores por defecto

Por defecto, el navegador establece valores iniciales a algunas propiedades CSS, este es el caso de margin y padding. Una buena práctica es utilizar el selector universal
para restablecer estos valores a 0, para que no surjan errores inesperados.

```
* {
    margin: 0;
    padding: 0;
}
```

### Tamaño total del elemento

El tamaño total del elemento está determinado por la suma de los valores de las propiedades border y width o height dependiendo del eje. La propiedad margin no esta icluida en este cálculo.

Por ejemplo, definimos los siguientes estilos:

```
div{
  width: 150px;
  height: 150px;
  padding: 20px;
  border: 10px solid gray;
  margin: 30px;
}
```

El tamaño total del elemento será de 210px en ambos ejes, donde la suma fue: 150 (altura/anchura) + 20 x 2 (padding ambos lados) + 10 x 2 (borde ambos lados). Si evaluamos este elemento en las herramientas del desarrollador mostrará su tamaño como 210x210.


### Propieada box-sizing

La propiedad box-sizing establece cómo se calcula el width y el height si incluyen bordes y espacions internos. como buena practica, se lo coloca en el selector universal, para que todos los elementos sigan esta tendencia

```
* {
  box-sizing: border-box;
}
```

Con el valor border-box, el tamaño total del elemento será igual al especificado en el width y height, provocando que las medidas del contenido cambien con respecto a los bordes y espacios internos.

El tamaño total del elemento será de 150px en ambos ejes, donde se calcularon las medidas del contenido para que la suma total sea lo especificado en el width y height. Si evaluamos este elemento en las herramientas del desarrollador mostrará su tamaño total como 150x150 y el contenido como 90x90.

### Problema con el tamaño de los bordes

Recapitulando, el tamaño total de un elemento es la suma de tres: el borde, el espacio interior y el contenido.

Entonces, en algunas ocasiones tendrás la intención de añadir un borde al realizar un hover. Esto provocará que el elemento necesite más espacio del inicial, en un contenedor con más elementos puede ocasionar un conflicto.

La solución a esto es colocar un borde de color transparent (transparente) y del mismo tamaño que el otro borde. Esto hará que el elemento se mantenga en su tamaño total, lo único que cambia es el color.

Ejemplo de como solucionar el error [Ejemplo border](https://codi.link/PGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KPGRpdj5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCBjb25zZWN0ZXR1ciBhZGlwaXNpY2luZyBlbGl0aTwvZGl2Pg0KDQoNCg==%7CLyogUXVpdGEgbG9zIGNvbWVudGFyaW9zIHkgb2JzZXJ2YSBsbyBxdWUgb2N1cnJlICovDQoqIHsNCiAgbWFyZ2luOiAwOw0KICBwYWRkaW5nOiAwOw0KfQ0KDQpkaXZ7DQogIGRpc3BsYXk6IGlubGluZS1ibG9jazsNCiAgYmFja2dyb3VuZC1jb2xvcjogZ3JlZW55ZWxsb3c7DQogIHdpZHRoOiAxNTBweDsNCiAgaGVpZ2h0OiAxNTBweDsNCiAgcGFkZGluZzogMjBweDsNCiAgbWFyZ2luOiAzMHB4Ow0KICAvKiBib3JkZXI6IDEwcHggc29saWQgdHJhbnNwYXJlbnQ7ICovDQp9DQoNCmRpdjpob3ZlcnsNCiAgYm9yZGVyOiAxMHB4IHNvbGlkIGdyYXk7DQogIGN1cnNvcjogcG9pbnRlcjsNCn0NCg0KDQoNCg0KDQo=%7C).

### Colapso de márgenes

El colapso de márgenes sucede cuando dos elementos bloque adyacentes tienen un determinado valor de margin, entonces estos márgenes se solapan en un solo valor, el mayor de ambos.

**Sucede cuando: Hay dons elementos bloque adyacentes**

**No sucede cuando: Flexbox, Grid y elementos que no sean bloque**