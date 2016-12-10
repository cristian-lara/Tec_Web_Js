# NPM
---

### Materia: `Tecnologías Web con JavaScript`
### Tema : `NPM` 
### Fecha : `2016-12-08`
### Estudiante : `Cristian Raul Lara Balarezo`
### Profesor : `Tania Calle - Adrian Eguez`
### Número de informe : `4`

<a name="Cabecera"></a>
## Índice de contenidos


- <a href="#Tema">Tema</a>
- <a href="#Objetivos">Objetivos</a>
- <a href="#Marco Teórico">Marco Teórico</a>
* <a href="#Node.js">Node.js</a>
* <a href="#Npm">npm</a>

- <a href="#Desarrollo">Desarrollo de la Práctica</a>
- <a href="#Conclusiones y Recomendaciones">Conclusiones y Recomendaciones</a> 

<a name="Tema"></a>
## Tema
`NPM`
<br>
<a href="#Cabecera">A la cabecera</a>

<a name="Objetivos"></a>
## Objetivos

- Utilizar Node.js para desarrollar aplicaciones que utilizan JavaScript mediante funciones.
- Manejar npm para compartir y reutilizar código.
- Crear paquetes con funcionalidad que puede ser reutilizada a futuro.
- Crear scripts para ejecutarlos en node
<br>

<a href="#Cabecera">A la cabecera</a>

<a name="Marco Teórico"></a>
## Marco Teórico


<a name="Node.js"></a>
### Node.js

* Node.js es un entorno de ejecución para JavaScript construido con el motor de JavaScript V8 de Chrome. 
* Usa un modelo de operaciones E/S sin bloqueo y orientado a eventos, que lo hace liviano y eficiente. 
* El ecosistema de paquetes de Node.js, npm, es el ecosistema mas grande de librerías de código abierto en el mundo.

(Fuente: [Node.js](https://nodejs.org/es/))
<br>
<a href="#Cabecera">A la cabecera</a>

<a name="Npm"></a>
### npm

* npm facilita a los desarrolladores de JavaScript compartir y reutilizar código, además de actualizar el mismo.
* Este código compartido es reutilizado por otros desarrolladores en sus propias aplcaciones para resolver problemsa particulares.
* Las partes de código reutilizable son llamados paquetes o módulos.
* Un paquete es un directorio con uno o más archivo él, que además tiempo un archivo llamado *package.json* con metadatos sobre el paquete.
* Una aplicación típica, como un sitio web, dependerá de decenas o cientes de paquetes.

(Fuente: [npm](https://docs.npmjs.com/getting-started/what-is-npm))
<br>
<a href="#Cabecera">A la cabecera</a>


<a name="Desarrollo"></a>
## Desarrollo de la práctica


1) Instalar Node.js. Para ellos accedemos al enlace [NodeJS](https://nodejs.org/es/) y hacemos clic en el botón mostrado.



2) Abrimos la consola (cmd) y ejecutamos el comando `node`.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node.JPG">
</p>

3) Ahora podemos utilizar código JS.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node2.JPG">
</p>

4) Salimos con *control+c* dos veces.

5) Nos movemos a la carpeta donde deseamos crear un paquete json y escribimos `npm init` para crearlo.

6) Llenamos la información que se nos pide y al final aceptamos con *yes*.
* Es importante tomar en cuenta que el campo *main* debe ser llenado como *app.js*.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node3.JPG">
</p>

7) Observamos que se ha creado un paquete JSON en nuestro computador. Si lo abrimos se muestra la información llenada anteriormente.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node4.JPG">
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node5.JPG">
</p>

8)  Procemos a crear un archivo llamado app.js (recordar que el campo main debía tener este nombre) con el siguiente código:


```javascript
var num1 = 1;
var num2 = 2;

var resultado = num1 + num2;

console.log(resultado);
```

9) Para ejecutarlo escribimos *nodo nombreArchivo*. En este caso *node app.js*
* Observamos que devuelve 3 (suma de num1 y num2).

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node6.JPG">
</p>

10) Para subir paquetes al internet debemos crear una cuenta en npm. Para ello vamos al enlace [Crear cuenta npm](https://www.npmjs.com/signup) y llenamos los campos pertinentes.

11) Ahora iniciamos sesión con esta cuenta. Usamos el comando `npm login` y llenamos los campos.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node7.JPG">
</p>

12) Podemos publicar el paquete con el comando `npm publish`.



13) En la página web, observamos que, efectivamente, el paquete ha sido publicado.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node8.JPG">
</p>

14) Para descargar un paquete usamos `npm install -g nombrepaquete`.
* Esta es una instalación global
* El paquete se instalará en la carpeta mostrada en consola.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node9.JPG">
</p>

14) Si queremos que el paquete se descargue en una carpeta que nosotros deseamos, usamos `npm install nombrepaquete`.
* Debemos movernos primero a dicha carpeta.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node10.JPG">
</p>

15) Observamos que efectivamente, el paquete se ha descargado.

<p align="center">
<img src="https://raw.githubusercontent.com/crisdiab/Tec_Web_Js/informeNPM/imagenes/node11.JPG">
</p>

16) Si se desea eliminar un paquete usamos `npm uninstall nombrepaquete`.

17) Ahora, vamos a importar un paquete. Para ellos vamos a modificar el código del segundo archivo *app.js*.

```javascript
module.exports = {
imprimirSuma1y2 : imprimirSuma1y2;

}

function imprimirSuma1y2() {
var num1 = 1;
var num2 = 2;

var resultado = num1 + num2;

console.log(resultado);

}
```
* Se ha creado una función *imprimirSuma1y2* que suma 1 y 2.
* *module.exports* nos va a permitir importar esta función.



<br>
<a href="#Cabecera">A la cabecera</a>

<a name="Conclusiones y Recomendaciones"></a>
## Conclusiones y Recomendaciones
* Se aprendieron conocimientos básicos sobre Node.js y npm.
* Se aprendió a utilizar Node.js y npm para crear y publicar paquetes con codigo funcional.
* Se recomienda leer la documentación original de las herramientas utilizadas para entender de mejor manera su utilización.
* Es necesario mantener sencillo el código para que pueda ser entendido por otros ademas de una buena documentacion para su utilizacion

<br>
<a href="#Cabecera">A la cabecera</a>

Autor: [Cristian Lara](https://github.com/crisdiab/)