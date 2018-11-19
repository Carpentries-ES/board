# Lineamientos de traducción  

Este será un documento compartido entre todos los traductores, donde podemos acceder a los lineamientos de traducción.
Por favor vayan agregando algunos lineamentos que consideren apropiados. Si necesitan discutir algún alineamiento contactarse con Hely o Paula.


## Atención
 - Idioma oficial: Español de latinoamerica (en si, por que la mayoría de los traductores son de latinoamerica)
 - Esta es una tradución en tono de voz informal
 - Vamos a tutear en las traducciones, decir "Tú" en vez de "vos" o "usted" y todas las conjugaciones de la persona "tú"
 - Usar "ustedes" en vez de "vosotros" y todas las respectivas conjugaciones
 - Ser cuidadosos con los acentos o tildes
 - Abrir y cerrar símbolos de pregunta y exclamación
 - Ortografía
 - Por defecto las traducciones llevarán género femenino (la-las-investigadoras-programadoras-etc) a fin de equilibrar el sesgo existente en la mayoría de los documentos, que usan el género masculino
 - Todos los números del cero al diez se escriben literalmente
 
## NO se traduce

- Los títulos en la cabecera de cada capítulo no se traducen, son símbolos de estilo (**title**, **objectives**, **keypoints**, etc.)
- {:.callout} y {: .challenge} Son símbolos de estilo
- Nombres de paquetes y funciones en R como ggplot2, tidyr, dplyr
- Nombres de variables en ejemplos y en general el código encerrado entre ~~~ ~~~ {: .bash},  {: .r}. Nota: Los comentarios dentro del código pueden traducirse si ven que al traducirlos las instrucciones serían más claras.
- Nombres de libros (referencias o citas)
- Nombres de programas
- Nombres de directorios o **paths**
- Nombres de la organización, por ejemplo **The Carpentries**, **Software Carpentry** and **Data Carpentry**
- Términos técnicos, pero hay que indicarlos en negrita (por favor ver abajo para más información), por ejemplo tipos de datos, se ha decidido no traducirlos.
- Imágenes, texto dentro de las imágenes, tampoco la referencia a donde se encuentra la imagen
- Nombres de roles, por ejemplo **Instructor**, **Maintainer**, **Trainer**


## Términos técnicos, no traducir sólo marcar con negrita o arregar `` ` `` si es una variable o parámetro

Por favor mantener orden alfabético

- **A**
    - el **array**
- **B**
    - sin artículo **bash**
    - el **bit score**
    - los **bytes**
    - el **branch**
- **C**
    - el **checkout**
    - sin artículo **commit**
    - el **cluster**
    - el tipo de datos **complex** en R
    - el tipo de datos **character** en R
- **D**
    - el **dataset**
    - el **dataframe** # en R
    - el `DataFrame` # en Python
    - el **Desktop**
    - tipo de datos **double**
    - un **docstring**
- **E**
   - el **e-value**
- **F** 
    - sin artículo **flag**
    - **false** / **FALSE**
    - **factor**
    - **float**
 - **G** 
    - **gapminder**
 - **H**
    - **home**
- **I**
    - el tipo de datos **integer**
- **L**
    - **list**
    - el tipo de datos **logical** en R
- **M**    
    - sin artículo **merge**
    - los **mismatches**
- **O**   
    - el **output**
- **P**   
    - el **password**
    - el **path**
    - un **pipe**
    - el **pipeline**
    - el **prompt**
    - sin artículo **pull**
    - sin artículo **push**
    - el **query**
    - el `pandas`
- **R**
    - sin artículo **root**
- **S**   
    - el **script**
    - el **set**
    - el **stage area**
    - el **subject**
- **T, U, V, W, X, Y, Z**   
    - el **timestamp**
    - el **username**
    - **true** / **TRUE**
    - tipo de datos **text**

Nota: me estoy dando cuenta que todos los anglicismos que hemos agregado van con artículo masculino el, a menos que sea un verbo.

## Términos técnicos a traducir - Glosario

Por favor mantener orden alfabético.
La columna de sinónimos está aquí sólo de referencia, son palabras aceptadas, pero usaremos la primera columna para la traducción.

|  Inglés 	| Español usar esta palabra | (sinónimos) |
|---	      |---	  |--- |
| **attendees**| participantes | asistentes|
| **browser**| Navegador de archivos | |
| **build** | construir el ejecutable | |
| **click**  	|  clic  	| |
| **command line**  	|  la línea de comandos  	| |
| **computer** 	    | computadora | ordenador  	|
| **contributer** |  contribuidor, no contribuyente||
| **Challenge** 	    | desafío	|reto|
| **dollar sign** 	    | signo `$`	| |
| **dry-run** 	    | ejecución "en seco" 	| |
| **environment variable**  | variable de entorno | |
| **file**   	|  archivo 	| |
| **input**   	|  entrada 	| |
| **legacy systems** 	|  sistemas obsoletos | sistemas heredados 	|
| **loop** 	|  bucle 	| |
| **output**   	|  salida (cuando se refiere a input-output) o resultado 	| |
| **plot** 	|  gráfico 	| |
| **quote** 	|  entrecomillar 	| |
| **run** 	|  ejecutar 	| |
| **refresh** | actualizar |
| **spreadsheet**  	|  planilla de cálculo  | |
| **shell**  	       |  la terminal  | la linea de comandos |
| **string**  	|  secuencia de caracteres -sólo se traduce si no es un tipo de datos  | |
| **self-contained** project| proyecto autónomo ||
| **tab completion**  | autocompletar	|autocompletado con el tabulador |
| **tip** / **hint** | sugerencia | consejo, pista|
| **trash bin**  | papelera de reciclaje	| |
| **version control**  	| control de versiones|  |
| **wild card**  | comodín  | caracter especial |
| **working directory** 	| directorio de trabajo | carpeta de trabajo 	|

## Fonología del código - cómo leerlo en voz alta

*Referencia* http://www.elcodigoascii.com.ar/

|  código 	| como al leer el código en voz alta |
| :---: | --- |
| ``` {} ``` | abre y cierra llaves curvas |
| ``` () ``` | abre y cierra paréntesis |
| ``` [] ``` | abre y cierra corchetes |
| ``` " ``` | comillas dobles|
| ``` ! ``` | signo de exclamación, signo de admiración |
| ``` # ``` | signo numeral, un **hashtag** |
| ``` / ``` | bara, barra inclinada, división|
| ``` \ ``` | barra invertida , contrabarra , barra inversa |
|  &#124; | barra vertical, pleca , linea vertical, un **pipe** |
| ``` * ``` | asterisco, comodín,	caracter especial |
| ``` ~ ``` | tilde, signo de equivalencia |
| ``` _ ``` | guión bajo|
| ``` . ``` | punto |
| ``` ` ``` | acento grave, **tick**|
| ``` $ ``` | signo de dólar, un **prompt** | 
| ``` + ``` | signo más, suma, positivo |
| ``` , ``` | coma |
| ``` - ``` | signo menos , resta , negativo , guión medio |
| ``` = ``` | signo igual, igualdad, igual que |
| ``` > ``` | mayor que | 
| ``` < ``` | menor que | 

