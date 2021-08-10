# Observaciones

Jose, felicitaciones por tu trabajo. Tu portfolio está muy hermoso, y se nota mucho el esfuerzo por lograr un trabajo con personalidad propia que a la vez cumpla las consignas y el diseño propuesto. El resultado es una web que te refleja y a la vez cumple a la perfección lo solicitado.

Como dije en clase, este trabajo no se hace para que constates conocimientos, sino para que aprendas: en ese sentido, mi intencion es que estos comentarios te sirvan para aprender, mejorar tu codigo a futuro e ir apreciando mejor qué se espera de nosotras como desarrolladoras front end.

La nota final no refleja tu trabajo, que es muy bueno, pero sí la ausencia de muchos pedidos de las consignas -favicon, deploy, readme adecuado. 

## Estructura correcta de documento HTML

Tu HTML esta muy bien. Claro, prolijo, muy bien comentado e identado.

Algo que me llama la atención es tu `header`, dado que allí repetís innecesariamente links.

```html
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
```

Cada uno de esos links hace exactamente lo mismo - traerse el css de google fonts para poder usar los fonts en tu sitio. Quizá estés bajo la impresión de que por cada uno de los fonts de tu web es necesario traerse nuevamente el css, pero no, no es necesario agregarlo más de una vez. Agregar muchos de estos links innecesarios impacta negativamente en la velocidad de carga de tu web, ya que por cada uno de ellos se hace un llamado a un css externo y se lo carga. 

Tenés tendencia a agregar divs innecesarios. Considerá por ejemplo tu navbar:

```html
    <header>
        <div class="conteinerMenu">
            <nav class="navBar">
                <ul>
```

La clase "conteinerMenu" se podria llevar a la etiqueta "header" y asi te ahorras un div que no necesitas. Te lo comento como ejemplo, pero esto se repite a lo largo de todo tu codigo. 

Utilizás la etiqueta ` <strong>` para darle grosor al texto: no llegué a comentarlo en clase, pero esto es incorrecto. Esa etiqueta es un resabio de viejas épocas en las cuales css no era tan poderoso como ahora, pero usarla hoy viola uno de los principios básicos de programación: la separación de responsabilidades. Los estilos se dan con css, la estructura se da con html. Una decisión de estilo como el grosor del texto debe controlarse con css, usando font-weight. 


## Respeta la consigna

- El portfolio cuenta con las secciones solicitadas

Cumplido, pero prestale atención a las mayúsculas. Escribir "proyectos" en minúscula o "conacto" en lugar de "Contacto" hace que tu web pierda profesionalidad, algo muy importante en un portfolio. 

- Al clickear en los links de navegación, debe llevar a la sección correspondiente

Cumplido

- Al clickear en los links de contacto, debe llevar a la página externa
  correspondiente

Cumplido, excepto por el email. Para agregar un link a un email usa el atributo `mailto`: `<a href="mailto: josefina@gmail.com">Email</a>` 

- El portfolio debe tener un diseño responsivo y verse correctamente en distintos dispositivos

Cumplido, con algunas excepciones. En celulares tus tarjetas de Mis Conocimientos se ven mal: esto es porque no eliminas el margen por defecto que traen los `<p>`, y eso provoca que corran de lugar al icono. En resoluciones para tablet el form no se ve bien. 

- El portfolio debe estar deployado y ser accesible desde una URL

Incumplido. 

- El repositorio en GitHub debe tener un readme adecuado

Incumplido. Los dos ultimos puntos son muy importantes para ir apuntando a la busqueda laboral. 

### Respeta el diseño dado

Cumplido.

### Buena estructura de proyecto

Cumplido. Notá que tenés una carpeta innecesaria, `vscode`, que es agregada a veces automáticamente por Visual Studio. Es buena práctica borrarla antes de una entrega. 

### Código bien indentado

Tabulas muy bien, lo cual parece un detalle extra cuando una recien comienza pero ayuda un monton a su legibilidad, y que lo hayas logrado en esta etapa es un gran mérito. 

### Comentarios que permiten mejorar la legibilidad del código

Impecables en HTML, lamentablemente ausentes en CSS, donde vendrían bien para separar los estilos de casa cosa.

### Uso correcto de etiquetas semánticas

En general, bien.  Me llama la atención que hayas usado `div` para las tarjetas de Mis Conocimientos y Mis Proyectos: yo diría que deberían ser `article`. Pero es el único detalle a comentar aquí (y hay quien podría discutirme que deberían ser divs). Tambien usas `article` para referirte a cada seccion: la etiqueta correcta alli es `section`. 

### Buenos nombres de clases

No usamos mayúsculas en HTML o CSS. Cuando quieras separar palabras, como en "navBar", escribilo con guiones: "nav-bar". 

Tus nombres de clases son descriptivos en sentido funcional, y me encanta ver lo bien que captaste esta idea.

### Código CSS bien estructurado

Cumplido a nivel formal. Noto algunos estilos innecesarios o confusos, que te voy indicando en tu archivo de css.

### Reutilización de estilos

Cumplido en general, veo que tuviste algunas dificultades. Tenes muchos estilos innecesarios, en particular muchiiiiiisimos width: 100% que son absolutamente innecesarios ya que ese es el comportamiento por defecto de los divs. alguna tarde tomate el ejercicio de volver a tu css y ver cuales de tus estilos son innecesarios - te vas a sorprender!

### Cumple con criterios básicos de accesibilidad

- Los colores tienen un contraste adecuado

Cumplido

- Las imágenes tiene el atributo `alt` que corresponde

Incumplido, la mayoria de los alt están vacíos. Eso sólo vale para imágenes decorativas. Me gusta el alt de la primera imagen. 

- Los íconos y elementos que no presentan texto agregan la información correspondiente por otros medios (etiquetas aria, texto oculto)

No cumplido, por ejemplo en los links a redes sociales de tu footer. Necesitan un aria.

- Los íconos y elementos que no necesitan ser anunciados por un lector de pantalla tienen la etiqueta aria
  correspondiente

No cumplido. 

- Commits con mensajes adecuados

Cumplido, noto muchos y buenos commits en tu proyecto, lo que siempre se agradece.

- Cuenta con un favicon

No cumplido. 

### Nota: 7
