---
title:  "Clean C# 5: condicionales"
date:   2022-03-09 08:00:00 -0500
categories: tutorial
comments: true
layout: csharp-tutorial
---

{: style="text-align: right" }
[Ir al inicio]({{ site.url }})

En este post, crearemos un programa que determine si una persona es mayor o menor de edad.

### Qué debemos hacer? Pensemos paso a paso

1. Primero necesitamos saber la edad de la persona
2. Tras tener la edad de la persona, debemos verificar el dato
* 2.1. Si la edad es mayor o igual a 18, la persona es mayor de edad
* 2.2. Si la edad es menor a 18, la persona es menor de edad
3. Debemos mostrar el resultado

Para verificar la edad, usaremos condicionales.

### Veamos cómo hacerlo:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=Console.WriteLine%28%2522Please%2520write%2520your%2520age%2522%29%253B%250Astring%2520ageAsText%2520%253D%2520Console.ReadLine%28%29%253B%250A%250Aint%2520age%2520%253D%2520Convert.ToInt32%28ageAsText%29%253B%250Aif%2520%28age%2520%253E%253D%252018%29%250A%257B%250A%2520%2520%2520%2520Console.WriteLine%28%2522You%2520are%2520an%2520adult%2522%29%253B%250A%257D%250Aelse%250A%257B%250A%2520%2520%2520%2520Console.WriteLine%28%2522You%27re%2520not%2520an%2520adult%2522%29%253B%250A%257D"
  style="width: 100%; height: 395px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### Analicemos el código:

- **Console.WriteLine("Please write your age:");** En esta línea mostramos un mensaje, que le dice al usuario que ingrese su edad.
- **string ageAsText = Console.ReadLine();** En esta línea creamos una variable, con el nombre ageAsText, y le asignamos el valor que ingrese el usuario, con el comando Console.ReadLine
    - **Console.ReadLine** toma el texto que el usuario escriba en la consola, retornando un string.
- **int age = Convert.ToInt32(ageAsText);** En esta línea **convertimos** la edad de string a int.
    - Recordemos que Console.ReadLine **sólo retorna strings**, por lo que debemos **hacer la conversión manualmente**.
    - **Convert** es una clase que nos ayuda a **convertir un tipo de dato, a otro tipo de dato**.
- **if (age >= 18)** En esta línea usamos un **condicional**, para verificar el **flujo a ejecutar**.
    - **if** es la sintaxis para crear un condicional.
    - **>=** es la sintaxis que usamos, para verificar si el dato de la izquierda, es **mayor o igual**, que el dato de la derecha.
- **else** se usa para indicar el código a ejecutar, en caso de que la condición del **if** no se cumpla.

### Mejoremos el código:

- Usar el valor 18, como lo estamos usando, no es la mejor idea. Este dato **"quemado" (hard-coded)**, hace el programa menos mantenible y escalable.
  - En el futuro, la mayoría de edad podría cambiar.
  - El programa no podría ser usado en otro país, donde la mayoría de edad sea a otra edad, por ejemplo, a los 21.
  - Además, en ciertos casos, al leer una variable "quemada" puede que no entendamos lo que signifique al instante, por lo que es mejor nombrarla.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=seti&wt=none&l=text%2Fx-csharp&width=680&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=true&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=const%2520int%2520AdultAge%2520%253D%252018%253B%250A%250AConsole.WriteLine%28%2522Please%2520write%2520your%2520age%2522%29%253B%250Astring%2520ageAsText%2520%253D%2520Console.ReadLine%28%29%253B%250A%250Aint%2520age%2520%253D%2520Convert.ToInt32%28ageAsText%29%253B%250Aif%2520%28age%2520%253E%253D%2520AdultAge%29%250A%257B%250A%2520%2520%2520%2520Console.WriteLine%28%2522You%2520are%2520an%2520adult%2522%29%253B%250A%257D%250Aelse%250A%257B%250A%2520%2520%2520%2520Console.WriteLine%28%2522You%27re%2520not%2520an%2520adult%2522%29%253B%250A%257D"
  style="width: 100%; height: 433px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### Qué hicimos?

- Creamos una **constante**, para guardar el valor de la mayoría de edad.
- Le dimos un nombre **descriptivo**, para que al leer el código, se **entienda** un poco más lo que se está haciendo

## Algunos comentarios sobre el código escrito:

- Las constantes **siempre** deben **empezar** con **mayúscula**, por convención.
- Para evitar valores "quemados", lo mejor siempre es obtenerlos de una **fuente de datos modificable**.
  - Del **Web.config**, un archivo de configuración que veremos más adelante.
  - O de una **base de datos**, **servicio**, **archivo** u otros medios, que veremos más adelante.
