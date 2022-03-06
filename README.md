# Proyecto-pd3 Puppy Web DAW Interfaces Web

## Enlace Netlify Despliegue

### https://pd3-puppy.netlify.app/


### Image edition
He utilizado GIMP para cambiar la escala a imagenes sobretodo de los background a más pequeñas, y a su vez, no he utilizado ninguna imagen de la página original debido a que en su mayoría se repetía la misma imagen siempre

## Reports LightHouse

### Home

![Report Home Lighthouse](./doc/home-lighthouse.jpg)

### About

![Report About Lighthouse](./doc/about-lighthouse.jpg)

## Ampliaciones

### SASS
Aunque en la rúbrica no se menciona como requisito, he decido utilizarlo para aprender como implementarlo con VueJs, de está forma saber como se aplicaría en un proyecto real.
Donde he aprovechado y aprendido como personalizar los estilos de los componentes brindados por bootstrap

### Bootstrap Icons
Si bien estaba Font Awesome, encontré que bootstrap también maneja su propia colección de iconos, y debido a que ya tenía configurado el proyecto para usarlo con bootstrap, esto me dio más facilidad en vez de tener de que configurar o install Font Awesome

### Más componentes
Según la rúbrica, basta con el Header y Footer, he decidido crear más componentes para diferentes utilidades los cuales he aprovechado para aprender mejor como crearlos con Vue y aplicando en algunos cierta lógica como el componente "DogCards" el cual hace un petición HTTP a una API de Perros para extrar información de distintos perros al rededor del mundo y usar esos datos para hacer una sección en la página donde tanto en este componente como en otros aprovechar el uso de distintos métodos o funciones que Vue tiene en su ciclo de vida para renderizar el contenido.
Donde también he aprovechado para incluir cierta lógica en el header respecto a los enlaces de navegación que usan Vue Router, donde si estás en la página actual, el enlace se opaca indicando que no lo puedes seleccionar porque ya estás en esa página, entre otras muchas cosas.

### Componentes de Vue
En mi travesía por entender mejor Vue me di cuenta que tienen una gran comunidad respecto al desarrollo de componentes de todo tipo, durante mi "investigación" encontré unos que consideré que podría mejorar el proyecto y mejorar la experiencía del usuario, entre estos están:

- Carousel / Slider: https://ismail9k.github.io/vue3-carousel/

- Video Background Responsive player: https://github.com/avidofood/vue-responsive-video-background-player

## Comandos para usar la app si haces git clone

```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```
