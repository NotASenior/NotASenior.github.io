---
layout: post
title:  "Clean C# 1: instalar Visual Studio"
date:   2021-06-21 09:43:56 -0500
categories: tutorial
comments: true
---

Lo primero que necesitaremos para programar con C#, es **Visual Studio**.
En realidad no lo necesitamos, ya que podemos usar comandos de consola para nuestros desarrollos. Pero instalar Visual Studio es mucho más **simple**, ya que apenas estamos empezando y no queremos complicarnos.

Ingresa a la siguiente URL [descargar Visual Studio](https://visualstudio.microsoft.com/es/)

Verás algo como esto:

![Instalar Visual Studio](/assets/images/1_InstallVS/1.jpg)

Pon el mouse sobre la opción **Descargar Visual Studio**, y aparecerán tres opciones.
Da clic en la versión **Community**, que es la versión gratuita.

Este ejecutable, es el **Visual Studio Installer**. Una herramienta que nos permite instalar el Visual Studio, y los componentes necesarios para desarrollar.

Al ejecutarlo, veremos lo siguiente:

![Instalar Visual Studio 2](/assets/images/1_InstallVS/2.jpg)

Da clic en continuar, y aparecerá un listado de características que podremos instalar. Algunas características podemos instalarlas después, a medida que las vayamos necesitando. 

Seleccionaremos las siguientes:

- Desarrollo de escritorio de .NET (necesario)
    - Con esta opción aprenderemos las bases del desarrollo
- Desarrollo de ASP.NET y web
    - Para el desarrollo de webs y APIs (ya veremos lo que es una API)
- Desarrollo multiplataforma de .NET
    - Para desarrollo con las últimas tecnologías, y orientado a soporte multiplataforma

![Instalar Visual Studio 3](/assets/images/1_InstallVS/3.jpg)

Una vez instalado, veremos la siguiente imagen:

![Instalar Visual Studio 4](/assets/images/1_InstallVS/4.jpg)

Hemos terminado de instalar Visual Studio. En la siguiente clase crearemos **nuestro primer proyecto**.

{% capture tmp %}{% include previous-next-post.md %}{% endcapture %}
{{ tmp | markdownify }}

{% capture tmp %}{% include comments.md siteUrl=site.url pageUrl=page.url %}{% endcapture %}
{{ tmp | markdownify }}
