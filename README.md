# intro_processing
#### HOLA MUNDO:

```js
void setup() {
  // Esta función se ejecuta una sola vez al inicio del programa.
  
  size(400, 400);
  // Define el tamaño de la ventana de visualización en 400x400 píxeles.
  
  background(255);
  // Establece el color de fondo de la ventana en blanco (255 en escala de grises).
  
  textSize(32);
  // Define el tamaño de la fuente del texto en 32 píxeles.
  
  fill(0);
  // Establece el color de relleno en negro (0 en escala de grises).
  
  text("Hola Mundo", 100, 200);
  // Dibuja el texto "Hola Mundo" en las coordenadas (100, 200).
}
```

En **Processing**, el método **void setup()** es una función fundamental que se utiliza para inicializar los valores y configuraciones del programa antes de que empiece a ejecutarse el bucle principal de dibujo, que está contenido en la función void draw().

###### Descripción más detallada de **void setup()**:

1.	Inicialización: void setup() se ejecuta una sola vez al comienzo del programa. Es el lugar ideal para inicializar variables, configurar el tamaño de la ventana, y establecer cualquier configuración inicial necesaria para el programa.
2.	Configuración de la Ventana: A menudo, se utiliza para definir el tamaño de la ventana de visualización con la función size(ancho, alto).
3.	Configuraciones Iniciales: Puedes definir el color de fondo inicial con background(), establecer el modo de color con colorMode(), y configurar otros parámetros como la velocidad de fotogramas con frameRate(), entre otros.

###### Ejemplo básico que muestra cómo se utiliza void setup():

```js 
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

```js
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


#### **CONCEPTOS BÁSICOS**.

##### I.	**Dibujar Formas Simples**:

•	Explicar la función size() para definir el tamaño de la ventana.
•	Introducir las funciones line(), rect(), ellipse() y point() para dibujar líneas, rectángulos, elipses y puntos.

```js
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
###### Por ejemplo: 
1.	line(:
	•	Este es el comando de Processing para dibujar una línea. La función line() requiere cuatro parámetros que especifican las coordenadas de los puntos inicial y final de la línea.
2.	50, 50,:
	•	Estos son los primeros dos parámetros de la función line(). El 50 primero es la coordenada x del punto inicial de la línea, y el segundo 50 es la coordenada y del punto inicial de la línea.
	•	En este caso, la línea comienza en el punto (50, 50) en la ventana de visualización.
3.	350, 350:
	•	Estos son los segundos dos parámetros de la función line(). El 350 primero es la coordenada x del punto final de la línea, y el segundo 350 es la coordenada y del punto final de la línea.
	•	En este caso, la línea termina en el punto (350, 350) en la ventana de visualización.
4.	);:
	•	Cierra la función line().

<img src="https://raw.githubusercontent.com/mauricixx/intro_processing/main/img/dibujar_linea_img.jpg"/>

En resumen, **line(50, 50, 350, 350)**; dibuja una línea que empieza en el punto (50, 50) y termina en el punto (350, 350). Estos puntos se refieren a coordenadas en la ventana de visualización de Processing, donde (0, 0) es la esquina superior izquierda y las coordenadas aumentan hacia la derecha y hacia abajo. La línea resultante es diagonal, yendo de la esquina superior izquierda a la inferior derecha dentro de los límites especificados.

#### Sistema de Coordenadas en Processing.

En Processing, el sistema de coordenadas de la pantalla es diferente al tradicional sistema de coordenadas cartesianas que se usa en matemáticas. Aquí está una explicación del por qué y cómo funciona este sistema en Processing:



##### 1.	Origen en la esquina superior izquierda:
•	En Processing, el punto (0, 0) está ubicado en la esquina superior izquierda de la ventana.
•	Esta convención proviene del diseño de gráficos en computadoras y pantallas, donde las coordenadas de los píxeles se cuentan a partir de la esquina superior izquierda.

##### 2.	Eje X:
•	El eje X aumenta hacia la derecha.
•	Esto es consistente con el sistema de coordenadas cartesianas.

##### 3.	Eje Y:
•	El eje Y aumenta hacia abajo.
•	Esto es opuesto al sistema de coordenadas cartesianas, donde el eje Y positivo va hacia arriba.
•	La razón para esto es histórica y práctica: las pantallas de las computadoras y los sistemas gráficos tempranos se diseñaron de esta manera, ya que es más intuitivo para representar imágenes y textos que se leen de arriba hacia abajo.

##### Razones Históricas y Prácticas

•	Pantallas de Raster:
•	Las pantallas de raster, que se utilizan en la mayoría de los monitores de computadora, escanean de izquierda a derecha y de arriba hacia abajo. Así que fue natural definir el origen en la esquina superior izquierda y hacer que las coordenadas y aumenten hacia abajo.
•	Facilidad de Uso en Gráficos:
•	Cuando se dibujan elementos gráficos y textos, a menudo es más conveniente empezar desde la parte superior de la pantalla e ir bajando, especialmente para interfaces de usuario, textos, y otras representaciones visuales que siguen un flujo de arriba hacia abajo.

##### Ejemplo Visual

##### Imaginemos una ventana de Processing de 100x100 píxeles:

•	El punto (0, 0) está en la esquina superior izquierda.
•	El punto (100, 0) está en la esquina superior derecha.
•	El punto (0, 100) está en la esquina inferior izquierda.
•	El punto (100, 100) está en la esquina inferior derecha.

```js
size(100, 100);
point(0, 0);     // Esquina superior izquierda
point(100, 0);   // Esquina superior derecha
point(0, 100);   // Esquina inferior izquierda
point(100, 100); // Esquina inferior derecha
```

<a href="https://mauricixx.github.io/intro_processing/cartesiano/index.html">Enlace para localizar puntos en un plano cartesiano y generar una línea.</a>

.___________________________________________________________________________________________________________________________________

##### II.	**Colores**:

•	Introducir background(), fill(), stroke() y noFill(), noStroke() para cambiar colores de fondo, relleno y contorno.

```js
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

* En Processing, la función **background()** se puede utilizar tanto en void setup() como en void draw(), pero cada ubicación tiene un propósito diferente y afecta el comportamiento de la animación de distintas maneras:

1.	Usar **background()** en **void setup()**:
	•	La función setup() se ejecuta una sola vez al inicio del programa.
	•	Si colocas background() en setup(), se establecerá un color de fondo al inicio y no se actualizará nuevamente durante la ejecución del programa. Esto significa que cualquier dibujo hecho en void draw() se acumulará sobre el fondo inicial, creando un efecto de superposición.

```js
void setup() {
  size(400, 400);
  background(200);  // El fondo se establece una sola vez al inicio
}

void draw() {
  ellipse(mouseX, mouseY, 50, 50);  // Los elipses se dibujan sobre el fondo sin borrarse
}
```

2.	**Usar background() en void draw():**
	•	La función draw() se ejecuta continuamente en un bucle, permitiendo la actualización constante de la pantalla.
	•	Si colocas background() en draw(), se establecerá el color de fondo en cada frame. Esto significa que cada nuevo dibujo en draw() se hará sobre un fondo limpio, creando la apariencia de movimiento y eliminando los dibujos anteriores.

```js
void setup() {
  size(400, 400);
}

void draw() {
  background(200);  // El fondo se actualiza en cada frame
  ellipse(mouseX, mouseY, 50, 50);  // Los elipses se dibujan y se "mueven" con el ratón
}
```

En resumen, usar background() en setup() establece un fondo fijo y todo lo que dibujes en draw() se acumulará sobre ese fondo. Usar background() en draw() actualiza el fondo en cada frame, creando un efecto de movimiento y eliminando los dibujos anteriores. La elección entre uno y otro depende del efecto visual que desees lograr en tu animación.


 ____________________________________________________________________________________________________________________

### <span style="color:green">**Interactividad.**</span>

##### I.	**Uso del Ratón**:

•	Introducir variables predefinidas como mouseX, mouseY.
•	Crear una simple interacción donde una forma sigue al ratón.

```js
void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  ellipse(mouseX, mouseY, 50, 50);
}
```

##### II.	 **Eventos del Ratón**:

•	Explicar mousePressed(), mouseReleased(), mouseDragged(), mouseMoved().
Estas funciones están diseñadas para detectar e interactuar con los eventos del ratón.

###### mousePressed()
```js
void mousePressed() {
  // Código que se ejecuta cuando se presiona un botón del ratón
}
```
1.	void mousePressed() {:
	•	Declara la función mousePressed(). Esta función se llama automáticamente cuando se presiona cualquier botón del ratón.
2.	// Código que se ejecuta cuando se presiona un botón del ratón:
	•	Dentro de esta función, puedes escribir cualquier código que deseas ejecutar cuando el ratón se presiona. Esto podría ser para iniciar una acción, como dibujar un punto o iniciar un arrastre.
3.	}:
	•	Cierra la función mousePressed().

###### mouseReleased()
```js
void mouseReleased() {
  // Código que se ejecuta cuando se libera un botón del ratón
}
```
1.	void mouseReleased() {:
	•	Declara la función mouseReleased(). Esta función se llama automáticamente cuando se libera cualquier botón del ratón.
2.	// Código que se ejecuta cuando se libera un botón del ratón:
	•	Dentro de esta función, puedes escribir cualquier código que deseas ejecutar cuando el ratón se libera. Esto podría ser para detener una acción iniciada por mousePressed(), como dejar de dibujar.
3.	}:
	•	Cierra la función mouseReleased().

###### mouseDragged()
```js
void mouseDragged() {
  // Código que se ejecuta cuando el ratón se mueve mientras se presiona un botón
}
```
1.	void mouseDragged() {:
	•	Declara la función mouseDragged(). Esta función se llama automáticamente cuando el ratón se mueve mientras se mantiene presionado cualquier botón del ratón.
2.	// Código que se ejecuta cuando el ratón se mueve mientras se presiona un botón:
	•	Dentro de esta función, puedes escribir cualquier código que deseas ejecutar mientras arrastras el ratón. Esto se usa comúnmente para dibujar o arrastrar objetos en la pantalla.
3.	}:
	•	Cierra la función mouseDragged().

mouseMoved()
```js
void mouseDragged() {
  // Código que se ejecuta cuando el ratón se mueve mientras se presiona un botón
}
```
1.	void mouseDragged() {:
	•	Declara la función mouseDragged(). Esta función se llama automáticamente cuando el ratón se mueve mientras se mantiene presionado cualquier botón del ratón.
2.	// Código que se ejecuta cuando el ratón se mueve mientras se presiona un botón:
	•	Dentro de esta función, puedes escribir cualquier código que deseas ejecutar mientras arrastras el ratón. Esto se usa comúnmente para dibujar o arrastrar objetos en la pantalla.
3.	}:
	•	Cierra la función mouseDragged().

mouseMoved()
```js
void mouseMoved() {
  // Código que se ejecuta cuando el ratón se mueve sin presionar ningún botón
}
```
1.	void mouseMoved() {:
	•	Declara la función mouseMoved(). Esta función se llama automáticamente cuando el ratón se mueve sin presionar ningún botón.
2.	// Código que se ejecuta cuando el ratón se mueve sin presionar ningún botón:
	•	Dentro de esta función, puedes escribir cualquier código que deseas ejecutar cuando el ratón se mueve libremente. Esto podría ser para actualizar la posición de un cursor o realizar una acción en función de la posición del ratón.
3.	}:
	•	Cierra la función mouseMoved().

###### Ejemplo de uso de estas funciones

Ejemplo completo que utiliza estas funciones para cambiar el color del fondo y dibujar círculos según las acciones del ratón:
```js
void setup() {
  size(400, 400);
  background(255);
}

void draw() {
  // Nada se actualiza continuamente en este ejemplo
}

void mousePressed() {
  fill(0, 0, 255); // Azul
  ellipse(mouseX, mouseY, 50, 50);
}

void mouseReleased() {
  fill(255, 0, 0); // Rojo
  ellipse(mouseX, mouseY, 50, 50);
}

void mouseDragged() {
  fill(0, 255, 0); // Verde
  ellipse(mouseX, mouseY, 50, 50);
}

void mouseMoved() {
  fill(255, 255, 0); // Amarillo
  ellipse(mouseX, mouseY, 50, 50);
}
```
###### En este ejemplo:

•	**mousePressed()** dibuja un círculo azul donde se presiona el ratón.
•	**mouseReleased()** dibuja un círculo rojo donde se libera el ratón.
•	**mouseDragged()** dibuja círculos verdes mientras se arrastra el ratón.
•	**mouseMoved()** dibuja círculos amarillos cuando el ratón se mueve sin presionar ningún botón.


###### Ejemplo de cómo cambiar el color de una forma cuando se presiona el ratón.

```js
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

```js
boolean isPressed = false;
```
1.	boolean:
	•	boolean es un tipo de dato en Java (y Processing) que puede tener uno de dos valores: true o false. Los valores booleanos se utilizan típicamente para representar condiciones o estados que pueden ser verdaderos o falsos.
2.	isPressed:
	•	isPressed es el nombre de la variable que estamos declarando. Este nombre puede ser cualquier identificador válido en Java, pero isPressed es un nombre descriptivo que sugiere que la variable se utilizará para verificar si algo está presionado o no (por ejemplo, una tecla o un botón).
3.	=:
	•	El operador de asignación = se utiliza para asignar un valor a una variable. En este caso, estamos asignando el valor false a la variable isPressed.
4.	false:
	•	false es uno de los dos valores posibles para un tipo de dato booleano. Aquí, indica que inicialmente, la condición representada por isPressed no es verdadera. Es decir, lo que sea que isPressed está representando (por ejemplo, si un botón está presionado), inicialmente no está ocurriendo.
5.	;:
	•	El punto y coma ; se utiliza para terminar la declaración en Java y Processing.

En resumen, boolean isPressed = false; declara una variable booleana llamada isPressed y le asigna el valor inicial false. Esto podría ser utilizado en un programa para rastrear si un botón, una tecla, o alguna otra condición está actualmente activa (presionada) o no. Por ejemplo, más adelante en el código podrías tener algo como:
```js
if (mousePressed) {
  isPressed = true;
} else {
  isPressed = false;
}
```
Esto actualizaría el valor de isPressed según el estado del ratón.



_________________________________________________________________________________________________________________________________________

#### Animación

##### I.	**Concepto de draw()**:

•	Explicar que la función draw() se ejecuta en un bucle continuo.
•	Crear una simple animación.

```js
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

##### II.	**Variables y Control**:

•	Introducir variables y estructuras de control como if, for, while.

```js
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

#### Guardar una imagen en Processing.

Para capturar y guardar una imagen en Processing, puedes usar la función save() o saveFrame() dependiendo de tus necesidades. Aquí te explico cómo utilizarlas:

##### 1. Guardar una Imagen en un Momento Específico

Si quieres guardar una imagen en un momento específico (por ejemplo, cuando se presiona una tecla), puedes usar la función save(). Este método guarda la pantalla actual como un archivo de imagen.

```js
void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  ellipse(mouseX, mouseY, 50, 50);
}

void keyPressed() {
  if (key == 's' || key == 'S') { // Presiona 'S' para guardar la imagen
    save("imagen_guardada.png");
  }
}
```

##### 2. Guardar una Secuencia de Imágenes

Si deseas capturar y guardar una secuencia de imágenes (por ejemplo, para crear una animación), puedes usar saveFrame(). Esta función guarda automáticamente una secuencia de imágenes numeradas.

```js
void setup() {
  size(400, 400);
}

void draw() {
  background(255);
  ellipse(mouseX, mouseY, 50, 50);

  // Guarda cada cuadro como una imagen numerada
  saveFrame("output/imagen-####.png");
}
```

##### En este caso, #### se reemplaza por el número del fotograma (por ejemplo, imagen-0001.png, imagen-0002.png, etc.).

Notas:

•	Asegúrate de que la carpeta donde se guardarán las imágenes (output/ en el ejemplo) exista. De lo contrario, Processing la creará automáticamente.
•	Los archivos de imagen se guardan en el mismo directorio donde se encuentra el sketch de Processing.

##### Capturar un video en Processing.

Guardar un video directamente desde Processing no es tan directo como guardar imágenes. Processing no tiene una función incorporada para exportar video, pero puedes usar la biblioteca Video Export para lograrlo. Aquí te muestro cómo hacerlo:

I. Instalación de la Biblioteca Video Export

1.	Abre Processing.
2.	Ve a Sketch > Import Library > Add Library….
3.	Busca Video Export y haz clic en Install.

II. Código para Guardar un Video

Una vez que hayas instalado la biblioteca, puedes usar el siguiente código para capturar y guardar un video:
```js
import com.hamoid.*;

VideoExport videoExport;

void setup() {
  size(640, 480);
  videoExport = new VideoExport(this, "output_video.mp4"); // Nombre del archivo de video
  videoExport.startMovie(); // Inicia la grabación del video
}

void draw() {
  background(255);
  ellipse(mouseX, mouseY, 50, 50);

  videoExport.saveFrame(); // Guarda cada cuadro en el video
}

void keyPressed() {
  if (key == 'q' || key == 'Q') {
    videoExport.endMovie(); // Finaliza la grabación del video al presionar 'Q'
    exit(); // Cierra el programa
  }
}
```

III. Explicación del Código

•	VideoExport videoExport;: Declara una variable para manejar la exportación de video.
•	videoExport = new VideoExport(this, "output_video.mp4");: Inicializa la exportación de video con el nombre del archivo donde se guardará.
•	videoExport.startMovie();: Comienza la grabación del video.
•	videoExport.saveFrame();: Guarda el cuadro actual en el video. Esta función debe ser llamada dentro de draw() para capturar cada fotograma.
•	videoExport.endMovie();: Termina la grabación del video y guarda el archivo. Puedes asociar esta función a una tecla, como se muestra en el ejemplo, para detener la grabación cuando lo desees.

IV. Notas Importantes

•	El video se guardará en la misma carpeta que contiene tu sketch de Processing.
•	Asegúrate de no omitir videoExport.endMovie();, ya que es necesario para finalizar y guardar el video correctamente.
•	Si tu sketch es largo o tiene un alto número de cuadros por segundo (fps), el archivo de video podría ser grande. Ajusta la calidad y duración según tus necesidades.
















