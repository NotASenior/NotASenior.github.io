---
layout: post
title:  "Clean C# 4: aprender a saludar"
date:   2021-06-21 09:47:56 -0500
categories: tutorial
---

Ahora, partiendo del programa que creamos en la **lección 2**, aprenderemos a saludar a cualquier persona.

Este es nuestro código actual.

![SolutionNaming](/assets/images/2_MyFirstProject/6.jpg)

Ahora, modifiquemos el código para que nos salude:

{% highlight csharp %}
Console.WriteLine("Hello Frank!");
{% endhighlight %}

El problema con el código anterior, es que debemos modificarlo cada vez que querramos saludar a alguien diferente. 
Para solucionar este problema, aprenderemos a pedir datos al usuario, y guardarlos en variables.

Veamos cómo hacerlo:

{% highlight csharp %}

Console.WriteLine("Write your name:");
string name = Console.ReadLine();

Console.WriteLine("Hello " + name);

{% endhighlight %}

Analicemos el código:

- **Console.WriteLine("Write your name:");** En esta línea mostramos un mensaje, que le dice al usuario que ingrese su nombre.
- **string name = Console.ReadLine();** En esta línea creamos una variable, con el nombre name, y le asignamos el valor que ingrese el usuario, con el comando Console.ReadLine
    - **Console.ReadLine** toma el texto que el usuario escriba en la consola, retornando un string.
- **Console.WriteLine("Hello " + name);** En esta línea mostramos un mensaje, saludando al nombre escrito en la variable.
    - **+** este operador, nos permite concatenar dos strings.

## Algunos comentarios sobre el código escrito:

 Pudimos haber llamado la variable de cualquier manera que quisieramos, por ejemplo: **n**, **text**, **value**; pero una de las **prácticas más importantes** a la hora de desarrollar, es **usar buenos nombres**.
 Cuando usamos buenos nombres, nuestro código es **más fácil de leer**, y nuestros compañeros (o incluso nosotros mismos en el futuro) podrán trabajar más fácilmente con nuestro código.

 En el futuro aprenderemos cómo mejorar nuestro código de otras maneras, como por ejemplo, separando responsabilidades.

{% capture tmp %}{% include previous-next-post.md %}{% endcapture %}
{{ tmp | markdownify }}