---
title:  "Clean C# 4: aprender a saludar"
date:   2021-06-21 09:47:56 -0500
categories: tutorial
comments: true
---

Ahora, partiendo del programa que creamos en la **lección 2**, aprenderemos a saludar a cualquier persona.

Este es nuestro código actual.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=Console.WriteLine%28%2522Hello%2520World%21%2522%29%253B"
  style="width: 100%; height: 191px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Ahora, modifiquemos el código para que nos salude:
<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=Console.WriteLine%28%2522Hello%2520Frank%21%2522%29%253B"
  style="width: 100%; height: 191px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

El problema con el código anterior, es que debemos modificarlo cada vez que querramos saludar a alguien diferente. 
Para solucionar este problema, aprenderemos a **pedir datos al usuario**, y **guardarlos en variables**.

Veamos cómo hacerlo:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=Console.WriteLine%28%2522Write%2520your%2520name%253A%2522%29%253B%250Astring%2520name%2520%253D%2520Console.ReadLine%28%29%253B%250A%250AConsole.WriteLine%28%2522Hello%2520%2522%2520%252B%2520name%29%253B"
  style="width: 100%; height: 246px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Analicemos el código:

- **Console.WriteLine("Write your name:");** En esta línea mostramos un mensaje, que le dice al usuario que ingrese su nombre.
- **string name = Console.ReadLine();** En esta línea creamos una variable, con el nombre name, y le asignamos el valor que ingrese el usuario, con el comando Console.ReadLine
    - **Console.ReadLine** toma el texto que el usuario escriba en la consola, retornando un string.
- **Console.WriteLine("Hello " + name);** En esta línea mostramos un mensaje, saludando al nombre escrito en la variable.
    - **+** este operador, nos permite concatenar dos strings.

### Ahora, saludemos con nombre y apellido

Qué debemos hacer? Pensemos paso a paso
1. Necesitamos una variable, dónde guardar el apellido
2. Necesitamos pedir el apellido, y guardarlo en la variable
3. Necesitamos mostrar el apellido, después del nombre, separado por un espacio

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=Console.WriteLine%28%2522Write%2520your%2520name%253A%2522%29%253B%250Astring%2520name%2520%253D%2520Console.ReadLine%28%29%253B%250A%250AConsole.WriteLine%28%2522Write%2520your%2520last%2520name%253A%2522%29%253B%250Astring%2520lastName%2520%253D%2520Console.ReadLine%28%29%253B%250A%250AConsole.WriteLine%28%2522Hello%2520%2522%2520%252B%2520name%2520%252B%2520%2522%2520%2522%2520%252B%2520lastName%29%253B%250A"
  style="width: 100%; height: 321px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

## Algunos comentarios sobre el código escrito:

Concatenar strings con el operador + **no es la mejor opción** a la hora de trabajar con strings, ya que esto genera un gasto de recursos adicional.
En estos momentos no es tan importante, pero más adelante veremos el impacto de concatenar strings de esta manera, y cómo hacerlo de una mejor manera.

Pudimos haber llamado la variable de cualquier manera que quisieramos, por ejemplo: **n**, **text**, **value**; pero una de las **prácticas más importantes** a la hora de desarrollar, es **usar buenos nombres**.
Cuando usamos buenos nombres, nuestro código es **más fácil de leer**, y nuestros compañeros (o incluso nosotros mismos en el futuro) podrán trabajar más fácilmente con nuestro código.

En el futuro aprenderemos cómo mejorar nuestro código de otras maneras, como por ejemplo, **separando responsabilidades**.

{% capture tmp %}{% include previous-next-post.md %}{% endcapture %}
{{ tmp | markdownify }}

{% capture tmp %}{% include comments.md siteUrl=site.url pageUrl=page.url %}{% endcapture %}
{{ tmp | markdownify }}