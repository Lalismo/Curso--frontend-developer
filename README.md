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


