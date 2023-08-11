# OOCSS
 Plantilla explicativa de la arquitectura OOCSS

Object-Oriented CSS (OOCSS) es una metodología de diseño y estructuración de hojas de estilo CSS que se centra en la creación de componentes reutilizables y modulares. SASS, por otro lado, es un preprocesador de CSS que te permite escribir CSS con características adicionales como variables, anidamiento y mixins. Puedes combinar OOCSS con SASS para crear un flujo de trabajo más eficiente y organizado. Aquí hay algunos pasos para utilizar la arquitectura OOCSS con SASS:

1. **Estructura de carpetas:**
   Organiza tus archivos de la manera que te resulte más conveniente. Por ejemplo:
   
   ```
   project/
   ├── styles/
   │   ├── base/
   │   ├── components/
   │   ├── layout/
   │   ├── themes/
   │   └── main.scss
   └── index.html
   ```

2. **Establece una base:**
   Crea una carpeta `base` para contener estilos que se aplicarán globalmente a todo el sitio. Esto podría incluir reseteos, tipografía básica y estilos de formularios.

3. **Componentes reutilizables:**
   En la carpeta `components`, crea estilos para componentes individuales como botones, tarjetas, barras de navegación, etc. Cada componente debe ser independiente y autocontenido, lo que significa que debería llevar su propio estilo y estructura.

4. **Diseño y disposición:**
   La carpeta `layout` podría contener estilos relacionados con la estructura general del sitio, como la disposición de encabezados, pies de página, columnas y cuadrículas.

5. **Temas y variaciones:**
   Si estás trabajando con diferentes temas o variaciones de estilos, podrías utilizar la carpeta `themes`. Aquí es donde puedes definir estilos específicos para diferentes aspectos visuales del sitio.

6. **Archivo principal SASS:**
   En el archivo `main.scss`, importa tus diferentes archivos de SASS, siguiendo la estructura que has creado. Por ejemplo:

   ```scss
   // Importar estilos base
   @import 'base/reset';
   @import 'base/typography';
   @import 'base/forms';

   // Importar componentes
   @import 'components/buttons';
   @import 'components/cards';
   // ...

   // Importar estilos de diseño
   @import 'layout/header';
   @import 'layout/footer';
   // ...

   // Importar temas
   @import 'themes/light';
   @import 'themes/dark';
   // ...
   ```

7. **Variables y Mixins:**
   Aprovecha las características de SASS, como variables y mixins, para hacer que tu código sea más modular y reutilizable. Puedes definir colores, tamaños, espaciados u otras propiedades comunes como variables, y crear mixins para estilos repetitivos.

8. **Compilación:**
   Finalmente, asegúrate de compilar tus archivos SASS en un archivo CSS regular que se enlace en tu página HTML.

Recuerda que la clave de OOCSS es la modularidad y la reutilización. Al seguir esta estructura y aprovechar las características de SASS, estarás creando estilos más organizados y mantenibles para tu proyecto.