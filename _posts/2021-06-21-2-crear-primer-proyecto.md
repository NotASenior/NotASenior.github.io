---
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

Al dar clic en siguiente, aparecerá la versión de .NET a usar, usaremos la opción recomendada al crear el proyecto. En mi caso, seleccionaré la versión 6.

.NET es un framework que nos ayudará a desarrollar nuestros diferentes proyectos.

![SolutionNaming](/assets/images/2_MyFirstProject/4.JPG)

Al dar clic en **"Create"**, se creará la solución.

En el explorador de soluciones, veremos la solución, el proyecto y la clase base creada.

![SolutionNaming](/assets/images/2_MyFirstProject/5.JPG)

Analicemos el código creado

![SolutionNaming](/assets/images/2_MyFirstProject/6.JPG)

- En la línea 2, veremos la instrucción ejecutada.
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