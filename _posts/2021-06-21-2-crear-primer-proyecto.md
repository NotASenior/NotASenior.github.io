---
layout: post
title:  "Clean C# 2: nuestro primer proyecto"
date:   2021-06-21 09:44:56 -0500
categories: tutorial
comments: true
---

Vamos a crear nuestro primer proyecto.
Al abrir Visual Studio, veremos las siguientes opciones:

![VisualStudioOptions](/assets/images/2_MyFirstProject/1.JPG)

Seleccionaremos la opción **"Crear un proyecto"**.
A continuación, seleccionaremos **"Aplicación de consola"** o **"Console Application"** en inglés.

![ConsoleApplicationSelection](/assets/images/2_MyFirstProject/2.JPG)

Ingresaremos el **nombre del proyecto** que deseemos, en mi caso "ConsoleApp".
Seleccionaremos la **ruta** donde se va a guardar la solución, y por último, el **nombre de la solución**, que en mi caso es "Training".

![SolutionNaming](/assets/images/2_MyFirstProject/3.JPG)

Al dar clic en siguiente, si tenemos instalado .NET 5, y la opción de seleccionar la versión, aparecerá una ventana donde podremos seleccionar la versión de .NET a usar. En mi caso usaré .NET 5.

![SolutionNaming](/assets/images/2_MyFirstProject/4.JPG)

Al dar clic en **"Create"**, se creará la solución.

En el explorador de soluciones, veremos la solución, el proyecto y la clase base creada.

![SolutionNaming](/assets/images/2_MyFirstProject/5.JPG)

Analicemos la clase creada

![SolutionNaming](/assets/images/2_MyFirstProject/6.JPG)

- En la **línea 5**, veremos la **definición de la clase**, cuyo nombre es "Program".
    - Después analizaremos a fondo, lo que es una clase.
- En las **líneas 6 y 11** veremos un par de llaves. Todo el contenido de la clase, debe estar dentro de estas llaves
    - Si escribimos código fuera de estas llaves, el código no pertenecerá a esta clase.
- En la **línea 7**, veremos la **declaración del método** de entrada.
    - Este método se ejecutará **automáticamente**, al ejecutar el programa.
    - Los métodos de entrada, tienen el nombre **Main**, y son estáticos por convención.
    - **static**: indica que el método es estático (lo que significa que no debe existir una instancia de la clase, para usar el método).
        - Después veremos qué es una instancia.
    - **void**: indica que el método **no retornará ningún valor** (Más adelante, veremos métodos que devuelven valores).
    - **Main** es el nombre del método.
    - **Dentro** de los paréntesis veremos los **parámetros** recibidos (no usaremos estos aún. Los veremos más a fondo después).
        - **string[]** es el **tipo** de parámetro.
        - **args** es el **nombre** del parámetro.
- En la línea 9, veremos la instrucción ejecutada.
    - **Console**: es una clase que nos permite **interactuar con la consola**.
    - **WriteLine**: es un método que nos permite **escribir en la consola**.
    - **"Hello World"** es el **valor** que estamos escribiendo en la consola.
        - Este tipo de datos, rodeado por comillas, se conoce como cadena de texto, o **string**.

Este es nuestro primer programa, que saludará a quien lo ejecute (al mundo por ahora).
Ejecutemos nuestro programa.

![SolutionNaming](/assets/images/2_MyFirstProject/7.JPG)

Este será el resultado:

![SolutionNaming](/assets/images/2_MyFirstProject/8.JPG)

En nuestra próxima clase, aprenderemos un poco más sobre variables, lo que nos ayudará a crear un programa para saludar a cualquier usuario, y no sólo al mundo.

{% capture tmp %}{% include previous-next-post.md %}{% endcapture %}
{{ tmp | markdownify }}

{% capture tmp %}{% include comments.md siteUrl=site.url pageUrl=page.url %}{% endcapture %}
{{ tmp | markdownify }}