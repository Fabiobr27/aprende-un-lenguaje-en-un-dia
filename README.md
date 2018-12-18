# Aprende un lenguaje de programación en un día (ejercicio voluntario para subir nota).

## Introducción

Cuando te sacaste el carnet de conducir, aprendiste las normas de circulación así como los fundamentos básicos para manejar un coche: volante, marchas, freno, acelerador, embrague, retrovisores... Seguramente, el coche que conduces ahora es diferente al que utilizaste para aprender a conducir, no obstante, lo puedes llevar sin problema. Cada coche tiene sus peculiaridades, pero quien sabe manejar un automóvil, puede adaptarse a las medidas, tacto y comportamiento de un vehículo en cuestión de horas.

Aprender a programar es como aprender a conducir. Si tienes una base sólida de programación y sabes manejar con soltura los tipos de datos, bucles, arrays, clases, métodos, etc. podrás pasar de un lenguaje a otro en un período relativamente corto, simplemente tendrás que adaptarte a la sintaxis y a las peculiaridades del nuevo lenguaje.

Con este ejercicio se pretende despertar el interés por otros lenguajes de programación distintos al que el alumno está estudiando como primer lenguaje.

Sigue los pasos que se indican a continuación.

## Creación del equipo

Este ejercicio se debe hacer en grupos de 3 alumnos. Uno de ellos será el representante del grupo.

## Forkea forkea

El representante del grupo debe hacer un *fork* de este repositorio para utilizarlo como base.

## Añadiendo colaboradores

El encargado del grupo deberá añadir como colaboradores del repositorio *forkeado* a los otros dos miembros, para trabajar todos sobre los mismos archivos. Cuando alguien es colaborador en un repositorio, puede hacer *push* a él sin necesidad de pedir permiso o hacer *pull request*.

Para añadir colaboradores hay que hacer click en la pestaña *Settings* y seleccionar luego *Collaborators* en el menú.

## Miembros del grupo

Escribe aquí los miembros del grupo. El primero es el representante o encargado.

* Fabio Benítez
* David Gómez
* Sergio Almagro

## Lenguaje de programación

El profesor llevará una cajita llena de papelitos con los nombres de distintos lenguajes de programación. Los encargados de cada grupo meterán la mano en la caja y sacarán dos papelitos, de los cuales el grupo elegirá uno. No se permite hacer intercambio de papelitos entre grupos.

Escribe el lenguaje de programación elegido por el grupo.

* Groovy

Los papelitos se han recortado de este [documento](lenguajes_de_programacion.pdf).

## Información sobre el lenguaje


El lenguaje groovy es un superconjunto del lenguaje java  , de hecho un archivo .java , se puede renombrar en uno .groovy y podría seguir funcionando (salvo algunas incompatibilidades ). Tiene otras características principales como tipado estático y dinámico , sintáxis nativa para la manipulación de listas y maps , clousures .... .
El compilador Groovy genera bytecodes Java estándard que pueden usarse dentro de cualquier proyecto Java. Además, la mayoría del código Java es sintácticamente válido en Groovy.
Aquí tenemos 2 de sus principales ventajas;

Uso de properties:


![ventaja1](https://user-images.githubusercontent.com/43671744/50143349-a78a4d00-02ac-11e9-9dce-dddb69419dd3.png)


Closures vs Lambdas:





![ventaja2](https://user-images.githubusercontent.com/43671744/50143430-dbfe0900-02ac-11e9-9a6d-595c51bce9a9.png)




Se creó en 2003 , su creador es  James Strachan ( un ingeniero de software ).

https://www.genbeta.com/desarrollo/mejora-tu-codigo-java-usando-groovy

## Herramientas de desarrollo

Hay varias opciones ; se puede instalar la consola de groovy desde su página oficial , usar el lenguaje en los diferentess IDE's o instalar el lenguaje en una máquina virtual . 

Enlace de descarga--http://groovy-lang.org/download.html

## Poniendo en práctica el lenguaje

Pon en práctica el lenguaje de programación realizando los siguientes ejercicios. Para cada uno de los ejercicios, pega el código fuente de la solución y una captura de pantalla.

### 1. ¡Hola mundo!

Realiza un programa que muestre por pantalla la frase **¡Hola mundo!**.


```groovy
println "¡Hola Mundo!"
```


![captura de pantalla 64](https://user-images.githubusercontent.com/43568460/50142847-5fb6f600-02ab-11e9-86d0-8dfbc7e3bbdd.png)


### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.

### 3. Arrays y números aleatorios

Realiza un programa que rellene un array (o una estructura similar) con 20 números enteros aleatorios entre 1 y 100 y que seguidamente los muestre por pantalla. A continuación, se deben pasar los números primos a las primeras posiciones del array y los no primos a las posiciones restantes. Muestra finalmente el array resultado.
```groovy
package Holamundo;
import java.util.Scanner;

int [] numero = new int [20];
int [] primo =  new int [20];
int [] Noprimo = new int [20];
int i;
int j;
int primos = 0;
int Noprimos= 0;
boolean esPrimo = false;


System.out.println("ARRAY ORDERNAR PRIMO")

for(i = 0 ; i<20; i++){
 numero[i] =(int) (Math.random()*100)
 esPrimo= true;
 for( j = 2 ; j < numero[i];j++){
   if(numero[i] % 2 == 0){
	 esPrimo = false;
   }
 }
   if(esPrimo){
  primo[primos++]=numero[i];
}else{
  Noprimo[Noprimos++]=numero[i]
 }
 }
 
 System.out.println("Array Original")
 
 for(i= 0 ; i <20; i++){
   System.out.println(numero[i]);
 }
 for (i = 0 ; i < primos+ Noprimos; i++){
   numero[i] = primo[i];
 }
 for (i = primos ; i < primos + Noprimos; i++){
  numero[i] = Noprimo[i - primos];
 }
		
 System.out.println("Array Cambiado")
 for(i = 0 ; i <20;i ++){
   System.out.println(numero[i])
   }
```
![captura de pantalla 66](https://user-images.githubusercontent.com/43568460/50147063-82e6a300-02b5-11e9-96ed-3bc7e2023f69.png)

![captura de pantalla 67](https://user-images.githubusercontent.com/43568460/50147106-985bcd00-02b5-11e9-81f8-1aec188fde9c.png)



## Presentación de resultados

Cada equipo explicará al resto de la clase lo aprendido durante la realización del ejercicio. Todos los miembros de cada equipo deben participar en la explicación. Se puede utilizar como material de base para la presentación el repositorio de GitHub.

## Recompensa

* Todos los alumnos que realicen correctamente la actividad tendrán 0'25 puntos extra en la nota del trimestre.

* Los miembros del equipo más votado ganarán un premio.

:star: Si te ha gustado este ejercicio, dale una estrellita al [repositorio original](https://github.com/LuisJoseSanchez/aprende-un-lenguaje-en-un-dia).

