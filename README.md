# Paleta de Colores - Dashboard Premium

Este proyecto utiliza una paleta de colores moderna, enfocada en la estética "Dark Mode" (Modo Oscuro) basada en tonos Slate y azules, sin incluir ningún degradado.

A continuación, los colores implementados y sus usos:

| Hexadecimal | Nombre Aproximado | Uso Principal |
| :--- | :--- | :--- |
| **`#0b1120`** | Slate 950 (Casi Negro) | Fondo del documento (body) |
| **`#0f172a`** | Slate 900 (Azul Oscuro) | Contenedor principal, hero section y fondo de las tarjetas |
| **`#1e293b`** | Slate 800 (Azul Grisáceo) | Barra lateral y la sección posterior de las tarjetas |
| **`#334155`** | Slate 700 (Gris Pizarra) | Bordes de las tarjetas, footer del sidebar, recuadro de logo texto |
| **`#3b82f6`** | Blue 500 (Azul Primario) | Cuadro de acento para la marca/logo en el sidebar |
| **`#94a3b8`** | Slate 400 (Gris Claro) | Texto para los enlaces de navegación |
| **`#e2e8f0`** | Slate 200 (Blanco Hueso) | Texto principal y textos descriptivos en las tarjetas |
| **`#ffffff`** | Blanco Puro | Título destacado principal (Hero) |


## Cómo incluir una imagen de fondo en una etiqueta

Para colocar una imagen de fondo (background) utilizando CSS, tal como se implementó en la cabecera principal, debes seguir estos sencillos pasos:

1. **Añade una clase a tu etiqueta HTML:**
   Asegúrate de que el contenedor donde irá el fondo tenga una clase (recuerda que en este proyecto usamos únicamente clases).
   ```html
   <header class="hero-section">
       <!-- Tu contenido -->
   </header>
   ```

2. **Enlázalo usando `background-image` en tu archivo CSS:**
   En tu hoja de estilos, llama a la clase y usa la propiedad `background-image` con la función `url()` para indicar la ruta de la imagen. 
   
   * **Origen de la imagen:** La imagen puede estar previamente descargada y guardada dentro de la misma carpeta de tu proyecto, o bien, puedes colocar una URL externa completa de una imagen que esté en internet.
   * **Uso de comillas:** Dentro de la función `url()`, el uso de comillas simples o dobles es **completamente opcional**. Es válido escribir `url(hero_bg.jpg)` sin comillas. Sin embargo, usar comillas es una buena práctica recomendada, especialmente si la ruta o el nombre del archivo contiene espacios o caracteres especiales.

   ```css
   .hero-section {
       background-image: url('hero_bg.jpg');
   }
   ```

3. **Controla la apariencia del fondo (Explicación de propiedades):**
   Por defecto, las imágenes de fondo se muestran en su tamaño original y se repiten infinitamente (como un mosaico) para rellenar el espacio. Para que la imagen luzca profesional y adaptada a la caja, usamos estas propiedades adicionales:

   * **`background-image`**: Es la propiedad principal que le ordena al contenedor qué imagen gráfica debe pintar de fondo.
   * **`background-size: cover;`**: Esta propiedad obliga a la imagen a crecer o encogerse hasta **cubrir el 100% de la caja** sin perder sus proporciones. Esto evita que la imagen se vea estirada o achatada. Si la caja y la imagen tienen proporciones diferentes, `cover` recortará el sobrante.
   * **`background-position: center;`**: Define el punto de anclaje de la imagen. Al establecerlo en `center`, nos aseguramos de que el centro exacto de la fotografía siempre esté alineado con el centro de la caja, garantizando que el recorte sea simétrico en los bordes.

   ```css
   .hero-section {
       background-image: url('hero_bg.jpg');
       background-size: cover;      
       background-position: center; 
   }
   ```
