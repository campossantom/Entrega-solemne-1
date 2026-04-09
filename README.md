# Entrega-solemne-1

## Presentación de Proyecto  
En este proyecto desarrollamos el uso del creative coding para desarrollar una obra personal a partir de un referente de arte abstracto  
en este documento mostramos el paso a paso y los resultados obtenidos en base al uso y aprendizaje de códigos de programación utilizados en  
P5.Js.

El primer paso fue encontrar una obra que llamase nuestra atención y responda al arte abstracto, en este caso utilizamos una obra vista el año  
2025 en la exposición del MAC (Museo de Arte Contemporaneo) "Abstractos, kineticos y cinéticos". La obra en cuestión se llama Recinto Alucinante (1961) y  
pertene al autor Cubano Mario Carreño que se radicó en Chile y fue participe del movimiento abstracto en Chile. 

![Recinto Alucinante](https://mac.uchile.cl/wp-content/uploads/2022/07/Carren%CC%83o.jpg)  

![

### Problemas y soluciones dentro del trabajo

En un inicio la primera dificultad se parte en el como resolver la redistribución, pero solo dejar fluir la imaginanción y una pieza que busque  
ser una reversión del mismo ayudo a resolver esto.  
Una vez desarrollada la idea, al traspasarlo a un papel milimetrado, surge la problematica respecto al pixelado y traslación al programa.
Esto se resolvió creando un canvas en Adobe Illustrator y rehaciendo la obra en este programa, aprovechando que cada nodo queda marcado y en el programa te  
entrega las coordenadas (X,Y) de manera exacta para así facilitar el proceso de traspaso al software P5.

El conflicto para replicar colores se resolvió con ayuda de la inteligencia artificial Claude.com para obtener los códigos RGB.  

El mayor conflicto de traspaso a la composición fue la utilización del arco, ya que la forma en la cuál aprendimos a generarlos, nos entrega la mitad de un círculo  
completo, por lo que se veía mucho más grande, esto se solucionó creando un rectangulo del color del fondo y posteriormente una línea para dejar la composición como se  
quería. Además el circulo fue probandose desde una coordenada Y en negativo.

### Link con el archivo de P5.Js   

[Archivo en P5.Js de la obra](https://editor.p5js.org/campossantom/sketches/lizYvFDVF)


## Código de nuestro archivo  en P5.Js  
Cada código esta en conjunto a su comentario respectivo.

function setup() {  
  createCanvas(500, 500); //tamaño del canvas en pixeles.  
  angleMode(DEGREES); //función para crear arcos con angulo.  
}
function draw() {  
  background(54, 106, 185); //color en RGB para establecer el fondo.    
  stroke(18, 18, 18); //color del contorno.  
  strokeWeight(15); //peso del contorno en pixel.  
  fill(54, 106, 185); //color azul cobalto en RGB.  
  square(0, 0, 500); //cuadrado color del fondo azul cobalto con borde negro.  
  noStroke(); //eliminar el contorno.  
  fill(18, 18, 18); //color negro en RGB.  
  quad(97, 23, 437, 479, 243, 414, 49, 479); //poligono irregular negro grande del lado izquierdo.  
  triangle(437, 23, 437, 479, 296, 224); //Triangulo grande de lado derecho  
  fill(210, 208, 196); //color blanco RGB  
  quad(392, 132, 392, 250, 296, 224, 360, 133); //poligono irregular superior blanco inserto en la figura triangular negra derecha grande.  
  quad(392, 250, 392, 355, 368.5, 355, 339, 302); //poligono irregular inferior color blanco inserto en la figura triangular negra derecha grande.  
  quad(216.8, 250, 266.2, 250, 345, 355, 233, 355); //poligono irregular blanco inserto en la figura negra izquierda grande.  
  fill(195, 30, 28); //color rojo cadmio en RGB.  
  quad(243, 250, 266.2, 250, 305.2, 302, 266, 302); //poligono irregular color rojo inserto dentro del poligono irregular blanco, figura central.  
  rect(137.5, 137.5, 9, 255.4); //rectangulo rojo paralelo al blanco en lado izquierdo.  
  fill(210, 208, 196); //color blanco arena en RGB  
  quad(154, 392.4, 172.5, 392.4, 172.5, 313, 154.7, 288.5); //mitad de rectangulo superior del lado izquierdo.  
  quad(154, 250, 154, 137.5, 172.5, 137.5, 172.5, 216); //mitad de renctangulo infeior del lado izquierdo.  
  fill(54, 106, 185); //color azul cobalto RGB.  
  quad(165, 211, 146.5, 277, 243, 414.6, 216, 244); //poligono irregular que simila ser parte del fondo.  
  fill(210, 208, 196); //color blanco arena RGB  
  circle(437, 211, 46); //circulo perfecto color blanco en lado derecho. superior, el radio no funcionó, se uso el diametro para obtener tamaño.  
  fill(203, 122, 42); //color amarillo ocre RGB  
  circle(437, 151, 46); //circulo perfecto color amarillo ocre en lado derecho bajo el blanco. mismo problema con el radio, uso de diametro.  
  fill(195, 30, 28); //color rojo cadmio RGB  
  arc(267, -10, 346, 320, 0, 180); //arco utilizando angleMode/(degree)  
  fill(54, 106, 185); //color azul cobalto RGB  
  rect(80, 0, 370, 23); //Rectangulo superior para cortar el arco y dar el espacio buscado para la obra  
  stroke(18, 18, 18); //color negro en RGB  
  strokeWeight(10); //peso de la línea en pixel  
  strokeCap(SQUARE); //corte en cuadrado para la línea  
  line(80, 2.5, 450, 2.5); //coordenadas en relación a donde se creó el cuadrado para tapar el arco.  
}

## 
