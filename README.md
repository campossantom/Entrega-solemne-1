# Entrega-solemne-1

##

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
