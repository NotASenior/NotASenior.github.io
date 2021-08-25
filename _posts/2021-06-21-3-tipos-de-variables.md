---
layout: post
title:  "Clean C#3 : tipos de variables"
date:   2021-06-21 09:46:56 -0500
categories: tutorial
---

Inicialmente debemos responder la pregunta, **¿qué es una variable?**

Las variables son **espacios de memoria**, que usamos para guardar datos.

Si vamos a trabajar con el nombre de un usuario, necesitaremos guardar ese nombre en una variable, para usarlo cuando sea necesario.

{% highlight csharp %}
string nombreDelUsuario = "Pepe";
{% endhighlight %}

## Analicemos el código anterior

Creamos una **variable** de **tipo string**, con el nombre **nombreDelUsuario**, y le asignamos el valor **"Pepe"**.
Este valor "Pepe" puede ser cambiado en cualquier momento, por otro valor, por eso el nombre "variable".

### ¿Y qué significa string?
**String** es el tipo de variable que usamos.

Las variables de tipo string, pueden guardar cualquier **cadena de texto**. En este caso, **"Pepe"** es una cadena de texto.

### ¿Y qué es nombreDelUsuario?
**nombreDelUsuario**, es el nombre que decidimos darle a la **variable**. Podemos ¡usar el nombre que querramos!


### ¿Qué otros tipos de variables hay en C#?

En realidad son muchos. Algunos básicos son:

- **int**: guarda números enteros (que no tienen decimales)
- **float**: guarda números de punto flotante
- **char**: guarda un caracter
- **string**: guarda cadenas de texto
- **bool**: guarda sólo dos valores. true (verdadero) o false (falso)

{% highlight csharp %}
int edad = 25;
bool esMayorDeEdad = true;
string nombreDelUsuario = "Pepe";
{% endhighlight %}

No te preocupes si no entiendes estos tipos de variables aún.
Íremos aprendiéndolos, a medida que vayamos necesitándolos.

{% capture tmp %}{% include previous-next-post.md %}{% endcapture %}
{{ tmp | markdownify }}