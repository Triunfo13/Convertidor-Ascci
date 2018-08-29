# Convertidor Ascci
**Este codigo es un codigo simple:** Basicamente lo que hace es tomar una imagen en cualquier formato de imagen
y lo transaforma en caracteres ***ASCII***, los pasos son los siguientes.

## Pasos del codigo
1.Leer la imagen del directamente del codigo 
***Importante: cambiar la ruta de la imagen en el siguiente codigo, ya que la sintaxix lee ruta local***
` try {
 image = ImageIO.read(new File("D:\\Archivos\\Generations\\Practicas\\ASCII\\src\\ascii\\starwars.jpg")); //ruta de la imagen donde se leera, es importante cambiar en cada computadora
       } `
       
2.Obtener los valores de RGB con el siguiente codigo
` for (int y = 0; y <image.getHeight(); y++) //Evaluando los pixeles del eje y
       {
        for (int x = 0; x < image.getWidth(); x++) //Evaluando los pixeles del eje x
        {
            Color pixelColor = new Color(image.getRGB(x,y)); // Obtiene os valores RGB
            gValue = (((pixelColor.getRed()*0.2989)+(pixelColor.getBlue()*0.5870)+(pixelColor.getGreen()*0.1140))); //Convierte la imagen del RGB a escala de grises
            area.append(valorascii(gValue));// Un metodo que dependiendo del valor en escala de grises determina que caracter ascii deberia poner
            Imprimir(valorascii(gValue));//Imprime como un appendChild
        }
        area.append("\n");//Salta a la siguiente linea`
        
3.Tranferirlo en escala de grises

4.Asignarle valor ***ASCII*** dependiendo de la escala de grises

5.Observar el resultado
