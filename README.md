# Entrega-solemne-2

# Coding Creative Ejercicios y relación crítica con el las problemáticas de genero

Nuestro proyecto se realizo en P5.Js utilizando todas las directrices señaladas, considerando las problemáticas que un proyecto de código refiere, aprender variantes, códigos y horas de aprendizaje. Más que centrarnos directamente en un trabajo tan potente visualmente y cargado de simbolismos, buscamos representar nuestro aprendizaje de código y lograr unir todos los elementos que se solicitaban para así con este ejercicio tener herramientas que nos permitan en un futuro desarrollar de manera paciente y crítica nuestros proyectos.

Así a través de este memorándum vamos a mostrar como desarrollamos y nos inspiramos para llegar a este lugar.

## Referentes

![img](https://i.pinimg.com/736x/49/81/bc/4981bc3d21e1b948a509f718067efdd5.jpg)
![img](https://i.pinimg.com/1200x/a2/50/b5/a250b584278fc15c607cd7ef01303a2c.jpg)
![img](https://i.pinimg.com/736x/bf/6e/bc/bf6ebcf38eb4a131daeb32f328f34f08.jpg)
![img](https://i.pinimg.com/736x/60/2a/c2/602ac205da9599594f16ef6789c10cdf.jpg)
![img](https://i.pinimg.com/736x/93/1b/71/931b711016945f02e05966e23c2be96b.jpg)
![img](https://i.pinimg.com/736x/e9/a1/5d/e9a15dab72621b52f29753bedf6abf3a.jpg)
![img](https://arc-anglerfish-arc2-prod-copesa.s3.amazonaws.com/public/FTFF6OE7JZEVFHJM2J7JSD5UT4.jpg)

### Primeros acercamientos

En primera instancia realizamos reuniones donde discutimos acerca de nuestro proceso, que queriamos lograr y como lo queriamos lograr. Pasamos por diversos procesos de código, la mayoría discutiendo sobre propuestas, creadas por nosotros y pasadas por IA. Algunas desechadas pero que nos ayudaron a entender como funcionaba el código. Además de apoyarnos directamente con los ejemplos dispuestos en los ppt para ejercicios de P5.js y los videos de The Coding Train en Youtube.

[Link de Youtube para Coding Train Mix Videos](https://www.youtube.com/@TheCodingTrain/videos)

Además adjuntos algunos links de ejercicios, perdimos uno que fue un mapa interactivo de latinoamerica pero que nos enseño a crear botones en el código con códigos propios. Solo quedó el código módificado por la IA pero nos digustó el resultado y lo descartamos.

[Link P5.Js Basquiat](https://editor.p5js.org/campossantom/sketches/aQoLIJpf-)
[Link P5.Js Ejercicio Latam](https://editor.p5js.org/campossantom/sketches/hdgMOCHeB)


### Problemas y soluciones dentro del trabajo

La mayoría de los problemas fueron como ir describiendo y empezar el código adentrandonos a problemas. Además de convencernos de una problematica y como abordarla de manera correcta en el código.

Llegamos a la tematica escuchando un a Pablo Chile, los gangsters también lloran y pensamos "los hombres no lloran" y ahí reflexionando nos cuestionamos la problematica de manera importante respecto a como los hombres y masculinidades no reflexionan sobre sus sentimientos y como esto nos provoca de manera social no hablar sobre nuestra emocionalidad y reprimir emociones, siendo estas desembocadas de maneras poco saludables, llegando inclusive hasta el suicidio. Así encontramos nuestra problematica, como el caos mental y el ruido social nos empujan a caer en un gris oscuro, donde ocultamos la emocionalidad. Además aprovechamos de utilizar referencia a la obra *¿ES USTED FELIZ?* de Alfredo Jaar, que nos pareció pertinente para el ejercicio.

Ya adentrandonos y buscando cumplir con todos los requerimientos nos costaba ir en acumulación, ya que para nosotros buscabamos simplificar lo más posible, sin embargo fuimos dejando de lado lo literal de la imagen y basandonos en simbolos de la cultura popular como lo son las "Smiley Face" que aparecen en un episodio de Los Simpson cuando Lise consume antidepresivos/ansioliticos, representando como necesitamos enajenar en ocasiones con agentes exogenos nuestras emociones y así taparlas. Sin embargo estas sin un tratamiento adecuado, no solucionan el problema y desenbocan en dependencia y caer a lo más bajo en algunas ocasiones. Los hombres por esto tienden a ser de las personas que más suicidios efectivos realizan a pesar de no ser los que más lo intentan. Esto es relevante y hay muchos estudios que invitamos a revisar.

Entorno al código mismo nos apoyamos directamente con los videos mencionados antes, los ppts de la clase y finalmente apoyarnos directamente con Claude.ia y Gemini respecto a dudas o correcciones del código. Esto es muy relevante porque para enteder el código no podiamos depender al 100% de la IA ya que nos entregaba lineas de texto complejas que no lograbamos entender, por lo que nuestra solución fue ir desarrollandolo en conjunto, aprovechando las pruebas gratuitas y la lectura compleja, solicitando explicaciones y correcciones cuando cosas no nos funcionaban. Es importante aclarar que este código era necesario no solo entenderlo con la IA, sino que saber explicarlo y aplicar su funcionamiento crítico, ya que la IA en muchas ocasiones no lograba entregarnos un código que funcionase con nuestros requerimientos. 

A pesar de eso logramos apoyarnos de manera concreta y la IA nos ayudó a integrar funciones nuevas que no sabiamos como aplicar y ya estabamos en blanco. Además nos enseño a agregar audios y visualizar de manera el proyecto.

### Link con el archivo de P5.Js   

[Archivo en P5.Js de la obra](https://editor.p5js.org/campossantom/sketches/eHFCjFWYY)

let colores; // Array que guardará los colores del fondo  
let smile; // Variable para la imagen de cara feliz  
let posicionesImagenes = []; // Array con posición/velocidad de cada imagen feliz  
let sad; // Variable para la imagen de cara triste  
let posicionesImagenes2 = []; // Array con posición/velocidad de cada imagen triste  
let porcentajeGris = 0; // Controla cuánto gris aparece en el fondo (0 a 1)  
let sonidoFeliz; // Variable para el audio feliz  
let sonidoTriste; // Variable para el audio triste/estática  
let audioIniciado = false; // Evita que el audio se reinicie en cada click  

function preload() {  
  smile = loadImage("smile.png"); // Carga la imagen de cara feliz  
  sad = loadImage("sadface.png"); // Carga la imagen de cara triste  
  sonidoFeliz = loadSound("feliz.mp3"); // Carga el sonido feliz  
  sonidoTriste = loadSound("estatica.mp3"); // Carga el sonido de estática  
}  

function setup() {  
  createCanvas(500, 500); // Crea el lienzo de 500x500 píxeles  
  colores = [ // Define la paleta de colores del fondo alegre  
    color(255, 0, 0), // Rojo  
    color(255, 220, 0), // Amarillo
    color(0, 60, 200), // Azul
    color(255), // Blanco
  ];
  noStroke(); // Elimina el borde de las figuras  
  frameRate(10); // Limita la animación a 10 fotogramas por segundo  
  for (let i = 0; i < 10; i++) { // Repite 10 veces para crear 10 imágenes felices  
    posicionesImagenes.push({ // Agrega un objeto al array con propiedades de cada imagen  
      img: smile, // Imagen asignada (cara feliz)  
      x: random(20, width - 60), // Posición horizontal aleatoria dentro del canvas  
      y: random(-500, 0), // Posición vertical aleatoria fuera del canvas (arriba)  
      velocidad: random(2, 6), // Velocidad de caída aleatoria  
      tam: random(130, 260), // Tamaño aleatorio de la imagen  
    });  
  }  
  for (let i = 0; i < 10; i++) { // Repite 10 veces para crear 10 imágenes tristes  
    posicionesImagenes2.push({ // Agrega un objeto al array con propiedades de cada imagen  
      img: sad, // Imagen asignada (cara triste)  
      x: random(20, width - 60), // Posición horizontal aleatoria dentro del canvas  
      y: random(-500, 0), // Posición vertical aleatoria fuera del canvas (arriba)  
      velocidad: random(2, 6), // Velocidad de caída aleatoria  
      tam: random(130, 260), // Tamaño aleatorio de la imagen  
    });  
  }  
}  

function draw() {  
  background(220); // Limpia el fondo con gris claro en cada frame  
  if (mouseIsPressed) { // Si el mouse está presionado, muestra el modo triste  
    if (porcentajeGris < 1) { // Si el gris aún no llegó al máximo  
      porcentajeGris += 0.008; // Aumenta gradualmente el nivel de gris  
    }  
    let size = 50; // Define el tamaño de cada cuadro del fondo  
    for (let x = 0; x < width; x += size) { // Recorre el canvas en columnas  
      for (let y = 0; y < height; y += size) { // Recorre el canvas en filas  
        fill(random(255)); // Rellena cada cuadro con un gris aleatorio (efecto estática)  
        rect(x, y, size, size); // Dibuja el cuadro  
      }  
    }  
    for (let i = 0; i < posicionesImagenes2.length; i++) { // Recorre todas las imágenes tristes  
      let p = posicionesImagenes2[i]; // Referencia al objeto de imagen actual  
      p.y += p.velocidad; // Mueve la imagen hacia abajo según su velocidad  
      if (p.y > height) { // Si la imagen salió por abajo del canvas  
        p.y = random(-200, 0); // La reinicia arriba fuera del canvas  
        p.x = random(20, width - 60); // Le asigna una nueva posición horizontal aleatoria  
      }  
      let ansiedadX = random(-5, 5); // Genera un temblor horizontal aleatorio  
      image(p.img, p.x + ansiedadX, p.y, p.tam, p.tam); // Dibuja la imagen con temblor  
    }  
    textSize(30); // Define el tamaño del texto  
    textAlign(CENTER); // Centra el texto horizontalmente  
    textStyle(BOLD); // Pone el texto en negrita  
    fill(255, 0, 0); // Color del texto: rojo  
    let shakeX = random(-3, 3); // Temblor horizontal del texto  
    let shakeY = random(-3, 3); // Temblor vertical del texto  
    text("YA NO PUEDES MÁS", 250 + shakeX, 250 + shakeY); // Dibuja el texto con temblor en el centro  
  } else { // Si el mouse NO está presionado, muestra el modo feliz  
    let size = 50; // Define el tamaño de cada cuadro del fondo  
    for (let x = 0; x < width; x += size) { // Recorre el canvas en columnas  
      for (let y = 0; y < height; y += size) { // Recorre el canvas en filas  
        if (random(1) < porcentajeGris) { // Con probabilidad igual al nivel de gris acumulado  
          fill(random(100, 160)); // Pinta el cuadro con un gris medio  
        } else {  
          fill(random(colores)); // Pinta el cuadro con un color aleatorio de la paleta  
        }  
        rect(x, y, size, size); // Dibuja el cuadro  
      }  
    }  
    for (let i = 0; i < posicionesImagenes.length; i++) { // Recorre todas las imágenes felices  
      let p = posicionesImagenes[i]; // Referencia al objeto de imagen actual  
      p.y += p.velocidad; // Mueve la imagen hacia abajo según su velocidad   
      if (p.y > height) { // Si la imagen salió por abajo del canvas  
        p.y = random(-200, 0); // La reinicia arriba fuera del canvas  
        p.x = random(20, width - 60); // Le asigna una nueva posición horizontal aleatoria  
      }  
      image(p.img, p.x, p.y, p.tam, p.tam); // Dibuja la imagen en su posición actual  
    }  
    push(); // Guarda el estado actual de transformaciones  
    translate(250, 250); // Mueve el origen al centro del canvas  
    rotate(frameCount); // Rota según el número de frame actual (gira continuamente)  
    rectMode(CENTER); // Hace que el rectángulo se dibuje desde su centro  
    fill(255, 0, 0); // Color del cuadro: rojo  
    rect(0, 0, 50, 50); // Dibuja el cuadro rotatorio en el centro  
    pop(); // Restaura el estado de transformaciones anterior  
    textSize(30); // Define el tamaño del texto  
    textAlign(CENTER); // Centra el texto horizontalmente  
    textStyle(BOLD); // Pone el texto en negrita  
    fill(0); // Color del texto: negro  
    text("¿ES USTED FELIZ?", 250, 250); // Dibuja el texto en el centro del canvas  
  }  
}  
  
function mousePressed() {  
  if (!audioIniciado) { // Solo la primera vez que se hace click  
    sonidoFeliz.loop(); // Inicia el sonido feliz en loop  
    sonidoTriste.loop(); // Inicia el sonido triste en loop  
    sonidoTriste.setVolume(0); // Comienza el sonido triste en silencio  
    audioIniciado = true; // Marca que el audio ya fue iniciado  
  }  
  sonidoTriste.setVolume(1, 0.2); // Sube el volumen del sonido triste en 0.2 segundos  
  sonidoFeliz.setVolume(0, 0.2); // Baja el volumen del sonido feliz en 0.2 segundos  
}  
  
function mouseReleased() {  
  sonidoTriste.setVolume(0, 0.3); // Baja el volumen del sonido triste en 0.3 segundos  
  sonidoFeliz.setVolume(1, 0.3); // Sube el volumen del sonido feliz en 0.3 segundos  
}  
  
## Código de nuestro archivo  en P5.Js  
Cada código esta en conjunto a su comentario respectivo.

## Mapa de flujo
<img width="1251" height="1600" alt="WhatsApp Image 2026-05-22 at 10 43 33" src="https://github.com/user-attachments/assets/cd0aced7-edce-4a77-8637-e9c822d326f1" />



