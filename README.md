# intro_processing

En Processing, el método void setup() es una función fundamental que se utiliza para inicializar los valores y configuraciones del programa antes de que empiece a ejecutarse el bucle principal de dibujo, que está contenido en la función void draw().

Aquí tienes una descripción más detallada de void setup():

	1.	Inicialización: void setup() se ejecuta una sola vez al comienzo del programa. Es el lugar ideal para inicializar variables, configurar el tamaño de la ventana, y establecer cualquier configuración inicial necesaria para el programa.
	2.	Configuración de la Ventana: A menudo, se utiliza para definir el tamaño de la ventana de visualización con la función size(ancho, alto).
	3.	Configuraciones Iniciales: Puedes definir el color de fondo inicial con background(), establecer el modo de color con colorMode(), y configurar otros parámetros como la velocidad de fotogramas con frameRate(), entre otros.

Aquí tienes un ejemplo básico que muestra cómo se utiliza void setup():
```
void setup() {
  // Configurar el tamaño de la ventana de visualización
  size(800, 600);
  
  // Establecer el color de fondo
  background(255);
  
  // Configurar el modo de color
  colorMode(RGB);
  
  // Configurar la velocidad de fotogramas
  frameRate(30);
}
```
1.	void setup() {:
	•	Declara la función setup(). Esta función se ejecuta una vez al inicio del programa y se utiliza para realizar configuraciones iniciales.
2.	// Configurar el tamaño de la ventana de visualización:
	•	Este es un comentario que describe la siguiente línea de código. Los comentarios no son ejecutados por el programa y se usan para explicar o anotar el código.
3.	size(800, 600);:
	•	Establece el tamaño de la ventana de visualización en 800 píxeles de ancho y 600 píxeles de alto.
4.	// Establecer el color de fondo:
	•	Comentario que describe la siguiente línea de código.
5.	background(255);:
	•	Establece el color de fondo de la ventana en blanco. El parámetro 255 corresponde al valor máximo de blanco en la escala de grises (0 es negro, 255 es blanco).
6.	// Configurar el modo de color:
	•	Comentario que describe la siguiente línea de código.
7.	colorMode(RGB);:
	•	Configura el modo de color a RGB (Rojo, Verde, Azul). Esto significa que los colores se especificarán en términos de sus componentes rojo, verde y azul.
8.	// Configurar la velocidad de fotogramas:
	•	Comentario que describe la siguiente línea de código.
9.	frameRate(30);:
	•	Configura la velocidad de fotogramas a 30 cuadros por segundo. Esto significa que la función draw() se ejecutará 30 veces por segundo.
10.	}:
	•	Cierra la función setup().

```
void draw() {
  // Dibujar un círculo en la posición del ratón
  fill(0);
  ellipse(mouseX, mouseY, 50, 50);
}
```
11.	void draw() {:
	•	Declara la función draw(). Esta función se ejecuta continuamente, una vez por cada fotograma, permitiendo la animación y la actualización continua de la pantalla.
12.	// Dibujar un círculo en la posición del ratón:
	•	Comentario que describe las siguientes líneas de código.
13.	fill(0);:
	•	Establece el color de relleno para las formas que se dibujen a continuación. El parámetro 0 corresponde al color negro en la escala de grises.
14.	ellipse(mouseX, mouseY, 50, 50);:
	•	Dibuja una elipse (círculo) en la posición actual del ratón (mouseX, mouseY). La elipse tiene un ancho y una altura de 50 píxeles. Como el ancho y la altura son iguales, se dibuja un círculo.
15.	}:
	•	Cierra la función draw().

En este ejemplo, setup() se utiliza para configurar la ventana de visualización, el color de fondo, el modo de color y la velocidad de fotogramas. Luego, draw() contiene el código que se ejecuta repetidamente para dibujar en la pantalla.
Este código crea una ventana de 800x600 píxeles con un fondo blanco y dibuja un círculo negro en la posición del ratón, actualizando la posición del círculo continuamente a medida que el ratón se mueve.

 ___________________________________________________________________________________________________________________________________



* Conceptos Básicos.

1.	Dibujar Formas Simples:
	•	Explicar la función size() para definir el tamaño de la ventana.
	•	Introducir las funciones line(), rect(), ellipse() y point() para dibujar líneas, rectángulos, elipses y puntos.

```
void setup() {
  size(400, 400);
}

void draw() {
  background(255); // Fondo blanco
  line(50, 50, 350, 350);
  rect(100, 100, 200, 200);
  ellipse(200, 200, 100, 100);
  point(200, 200);
}
```

 ___________________________________________________________________________________________________________________________________


2.	Colores:
	•	Introducir background(), fill(), stroke() y noFill(), noStroke() para cambiar colores de fondo, relleno y contorno.

```
void setup() {
  size(400, 400);
  background(255);
}

void draw() {
  fill(255, 0, 0); // Color rojo
  rect(100, 100, 200, 200);

  noFill(); // Sin relleno
  stroke(0, 0, 255); // Contorno azul
  ellipse(200, 200, 100, 100);
}
```

 ___________________________________________________________________________________________________________________________________

Interactividad.

1.	Uso del Ratón:
	•	Introducir variables predefinidas como mouseX, mouseY.
	•	Crear una simple interacción donde una forma sigue al ratón.

```
void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  ellipse(mouseX, mouseY, 50, 50);
}
```

2.	Eventos del Ratón:
	•	Explicar mousePressed(), mouseReleased(), mouseDragged(), mouseMoved().
	•	Ejemplo de cómo cambiar el color de una forma cuando se presiona el ratón.

```
boolean isPressed = false;

void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  if (isPressed) {
    fill(0, 255, 0); // Verde
  } else {
    fill(255, 0, 0); // Rojo
  }
  ellipse(mouseX, mouseY, 50, 50);
}

void mousePressed() {
  isPressed = true;
}

void mouseReleased() {
  isPressed = false;
}
```

Animación

1.	Concepto de draw():
	•	Explicar que la función draw() se ejecuta en un bucle continuo.
	•	Crear una simple animación.

```
float x = 0;

void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  ellipse(x, height/2, 50, 50);
  x += 2; // Mover hacia la derecha
  if (x > width) {
    x = 0; // Reiniciar posición
  }
}
```

2.	Variables y Control:
	•	Introducir variables y estructuras de control como if, for, while.

```
int y = 0;

void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  for (int i = 0; i < width; i += 50) {
    ellipse(i, y, 25, 25);
  }
  y += 2;
  if (y > height) {
    y = 0;
  }
}
```












