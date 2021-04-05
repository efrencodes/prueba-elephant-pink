# 🎉 Prueba técnica para Elephant-Pink

## 📱 [Live Review](https://elephant-pink.efrenmartinez.dev/)
## 📋 [Repositorio](https://github.com/efrenmartinez/prueba-elephant-pink)

## 📦  Instalación

> NOTA: USÉ MAC PARA DESARROLLAR LA PRUEBA.

1. Se necesita clonar el repositorio desde GITHUB:

```bash
$ git clone https://github.com/efrenmartinez/prueba-elephant-pink.git
```

2. Acceder a la carpeta *prueba-elephant-pink*.

```bash
$ cd prueba-elephant-pink
```

3. Instalar las dependencias. Se puede usar [NPM](https://www.npmjs.com/) o [YARN](https://yarnpkg.com/). Correr el siguiente comando:

```bash
$ npm install
// or
$ yarn install
```

4. Para correr el proyecto, ejecutar el comando:

```bash
$ npm run dev
// or
$ yarn dev
```
## 📖 Contenido

Para la prueba me pedieron ciertos puntos a considerar:

* El proyecto debe estar desarrollado en VueJS.
* No usar un framework de CSS.

En este caso decidí usar y configurar el proyecto de esta manera:

* **NuxtJS** permite crear sitios estáticos.
* **SASS** para escribir CSS.
  * Carpeta assets/scss:
    * Está carpeta de encuentra dividido en diferentes carpetas y archivos:
        * Carpeta Components
          * Estilos de los componentes principales del sitio como butones, cards, icons, modal.
        * Carpeta base
            * base.scss
              * Estilos generales de la página.
            * typography.scss
              * Estilos para la tipografia
            * root.scss
              * Declaración de variables para los colores del sitio.
* **Cloudinary** es un servicio de CDN para hospedar las imagenes y las fuentes. Cloudinary se encarga de comprimir, optimizar las imágenes en automático.
* **Vercel** es un servicio de hosting gratuito para desplegar sitios estáticos. Con integración sencilla con diferentes frameworks de JavaScript.

## Bugs
Graves:

    Faltan los indicadores del slider (rombos).
    Falta la barra de copyright.

Medios:

    Barra superior: menú no alineado, márgenes incorrectos, estilo incorrecto en la caja de idiomas.
    Slider: flechas no alineadas con el menú superior, márgenes incorrectos, altura del slider incorrecta.
    Colección: no se usa el store para la colección de diamantes ni se controla de forma dinámica el número de elementos a mostrar sino que se repite el mismo elemento estático en dos bucles.
    Contacto: no hay validación de campos, los márgenes son incorrectos, no se ha hecho el estilo de input activo.

Leves:

    Los botones no tienen el estilo de fuente apropiado.
    El box-shadow del modal de contacto está mal.

Mejorables:

    El logo de DIAMOND no es clicable (ni siquiera es un enlace)
    Versión responsive inexistente, página totalmente descuadrada en la versión móvil.
    El slider no tiene eventos touch/drag para cambiar de diapositivas.
    El modal no se cierra al hacer click en el fondo negro.
