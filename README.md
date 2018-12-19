# Groovy

## Miembros del grupo

* Fabio Benítez
* David Gómez
* Sergio Almagro


## Introducción

James Strachan habló por primera vez sobre el desarrollo de Groovy en su blog en agosto de 2003. En marzo de 2004, Groovy se presentó al JCP como JSR 241 y se aceptó mediante votación.

El lenguaje groovy es un superconjunto del lenguaje java  , de hecho un archivo .java , se puede renombrar en uno .groovy y podría seguir funcionando (salvo algunas incompatibilidades ). Tiene otras características principales como tipado estático y dinámico , sintáxis nativa para la manipulación de listas y maps , clousures.

El compilador Groovy genera bytecodes Java estándard que pueden usarse dentro de cualquier proyecto Java. Además, la mayoría del código Java es sintácticamente válido en Groovy.
Se creó en 2003 , su creador es  James Strachan ( un ingeniero de software ).
Aquí tenemos 2 de sus principales ventajas:

Uso de properties:


![ventaja1](https://user-images.githubusercontent.com/43671744/50143349-a78a4d00-02ac-11e9-9dce-dddb69419dd3.png)


Closures vs Lambdas:





![ventaja2](https://user-images.githubusercontent.com/43671744/50143430-dbfe0900-02ac-11e9-9a6d-595c51bce9a9.png)





https://www.genbeta.com/desarrollo/mejora-tu-codigo-java-usando-groovy

## Herramientas de desarrollo

Hay varias opciones ; se puede instalar la consola de groovy desde su página oficial , usar el lenguaje en los diferentes IDE's o instalar el lenguaje en una máquina virtual . 

Enlace de descarga--http://groovy-lang.org/download.html



### 1. ¡Hola mundo!

Realiza un programa que muestre por pantalla la frase **¡Hola mundo!**.


```groovy
println "¡Hola Mundo!"
```


![captura de pantalla 64](https://user-images.githubusercontent.com/43568460/50142847-5fb6f600-02ab-11e9-86d0-8dfbc7e3bbdd.png)


### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.
```groovy
package HolaMundo;

print "Introduzca numero de filas: "
Scanner scan = new Scanner(System.in);

def numFilas =scan.nextLine() as Integer
 
System.out.println();
for(int altura = 1; altura<=numFilas; altura++){
	//Espacios en blanco
	for(int blancos = 1; blancos<=numFilas-altura; blancos++){
		System.out.print(" ");
	}
	 
	//Asteriscos
	for(int asteriscos=1; asteriscos<=(altura*2)-1; asteriscos++){
		System.out.print("*");
	}
	System.out.println();
}
```
![captura de pantalla 68](https://user-images.githubusercontent.com/43568460/50147356-3b144b80-02b6-11e9-98ea-ca36907343a7.png)



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



