# Scope
The scope of this repository consists of providing a set of functions programmed in the software
Engineering Equation Solver ([EES Overview](https://fchartsoftware.com/ees/)) for those interested
in following a heat and mass transfer course that uses as a guidebook the text *Heat and Mass Transfer:
Fundamentals and Applications* ([Google Books Overview](https://books.google.com.co/books/about/Heat_and_Mass_Transfer.html?id=6KmezQEACAAJ&source=kp_book_description&redir_esc=y)).

The code is provided as a native EES library file (.LIB), so it only needs to be imported as an external
library, and as a plain text file (.TXT) for easier visualization.

As of today, the repository contains two libraries:

* **heat_mass_transfer_user_1.LIB**: Covers the content from chapters 1 and 3 of the guidebook,
  *Introduction and Basic Concepts*, and *Steady-State Heat Conduction*.

* **heat_mass_transfer_user_2.LIB**: Currently contains content related to chapter 7, *External Forced Convection*.

The file names were chosen considering the number of exams in the course (usually 2 or sometimes 3).
Additionally, a configuration file is provided to enhance the visualization of the EES syntax (which is based on FORTRAN)
for better readability when using Notepad++ ([Notepad++ Overview](https://notepad-plus-plus.org/)):

* **config_UDL_EES.xml**

# Configuration

The following programs are used in a **Windows 10 Home V22H2 OS build 19045.5011 (X64) system**:
* **EES Professional V10.561**
* **Notepad++ V8.7**

# Usage

## Calling Libraries

To use any of the functions, subroutines, modules, or procedures contained in the libraries, simply include the
following line of code:
```Fortran
$Include FileLib$
```
Where the `string` variable, `FileLib$`, refers to the absolute path of the library file.  
It only needs to be included **once** to access its contents.

### Note

It is also possible to import the library through EES. To do this, simply initialize the `string` variable as an
empty string (`''`). A window will appear requesting the selection of the corresponding file, as indicated in the
internal EES documentation (*insert appropriate citation*).

![prompt_load_library](./visual_resources_docs/load_library_from_ees.png)

In my case, whenever I use this method, the extracted path is not correctly enclosed in apostrophes (`'`).  
It is necessary to manually adjust the path by placing it correctly between apostrophes, as this issue causes a compilation error.

![path_string_problem](./visual_resources_docs/load_library_from_ees_problem_w_path_and_var_str.png)

## Viewing Functions

Once the desired library has been loaded, to visualize its contents, open the **Function Info** section (in the
English version of EES[^bignote]) and click on **EES library routines**. In the list below, the name of the
previously loaded file will appear. Double-clicking it will display its contents.  
From this point forward, the usage flow is the same as for the built-in functions in EES.

![library_content_visualization](./visual_resources_docs/library_selection_from_function_info.png)

[^bignote]: This is the language setting of my EES version.  
    For clarification, all instructions and references within the program interface will be provided in English.

# TODO
* Update the libraries related to **convection**, considering what is natively available in EES.  
  Based on the evaluation, the following features are missing from the *Heat Transfer & Fluid Flow* module:
    * A function to calculate power given a pressure drop $\Delta P$ (*insert book citation*).
    * etc.
* Continue documentation in the README.
-------------------------
# Alcance
El alcance de éste repositorio consiste de facilitar de 
un conjunto de funciones programadas en el software 
Engineering Equation Solver ([EES Overview](https://fchartsoftware.com/ees/)) a 
quienes se encuentren interesados en seguir un curso de 
transferencia de calor y masa que utilice como libro guía 
el texto de Transferencia de calor y masa: fundamentos y 
aplicaciones principalmente ([Google books Overview](https://books.google.com.co/books/about/Heat_and_Mass_Transfer.html?id=6KmezQEACAAJ&source=kp_book_description&redir_esc=y)).

El código se encuentre plasmado, como archivo de librería 
nativo de EES (.LIB), para que no reste más que importarlo 
como una librería externa, y, como archivo de texto plano 
(.TXT) para una visualización más fácil.

Hasta hoy, el repositorio cuenta con 2 librerías:

* heat_mass_transfer_user_1.LIB: se encuentra lo 
correspondiente a los capitulos 1 y 3 del libro guía, 
Introducción y conceptos básicos, y, Conducción de calor 
en estado estable.

* heat_mass_transfer_user_2.LIB: por ahora, lo correspondiente 
al capitulo 7, Convección forzada externa.

El nombre de los archivos fue escogido teniendo en cuenta 
la cantidad de exámenes en el curso (2, a menudo, o, 3). Además, 
se proporciona un archivo para configurar, en parte, 
la visualización adecuada de la sintáxis EES (con base en 
FORTRAN), usada a lo largo de todo el código para revisión 
más ágil del código en el editor de texto Notepad++ 
([Notepad++ Overview](https://notepad-plus-plus.org/)): 

* config_UDL_EES.xml

# Configuracion

Los programas listados a continuación son para un sistema 
X64 en Windows 10 Home V22H2 OS build 19045.5011: 
* EES Professional V10.561
* Notepad++ V8.7

# Utilización

## Llamado de librerías

Para utilizar cualquiera de las funciones, subprogramas, modulos, procedimientos, contenidos 
en las librerías, basta con utilizar la siguiente línea de código:
```Fortran
$Include FileLib$
```
Donde la variable tipo ``` string ```, ``` FileLib$ ```, hace referencia a la ruta absoluta de la librería. 
Basta con realizar el llamado una sola vez para poder invocar su contenido.
### Nota

También es posible importar la librería a través de EES. basta con inicializar la variable tipo ``` string ``` 
vacía, usando ``` '' ```. Se desplegará una ventana solicitando que se seleccione el archivo en cuestión, tal 
cual como se es indicado en la documentación interna de EES (*insertar cita correspondiente*).
![prompt_load_library](.\visual_resources_docs\load_library_from_ees.png)
En mi caso, siempre que utilizo éste método, la ruta extraida no queda debidamente insertada entre los 
apóstrofes ('). Es necesario arreglarlo poniendo de manera correcta la ruta entre los apóstrofes, pues 
provoca un error de compilación.
![path_string_problem](.\visual_resources_docs\load_library_from_ees_problem_w_path_and_var_str.png)
## visualización de las funciones

Previa carga de la librería de interés, para visualizarla, hay que abrir la sección de Function Info 
(en la versión en inglés de EES[^bignote]), y clickar en EES library routines. en la lista justo 
abajo, aparecerá el nombre del archivo que se cargó anteriormente. Con doble click se despliega su 
contenido. De aquí en adelante, el flujo de uso es igual que con las funciones prestablecidas en 
EES.
![library_content_visualization](.\visual_resources_docs\library_selection_from_function_info.png)

[^bignote]: es el idioma en que tengo configurado mi versión de EES. 
    Como aclaración, las indicaciones y referencias dentro del canvas 
    del programa serán indicados mediante sus nombres en inglés.

# TODO
* Actualizar las librerías referentes al capitulo de convección, teniendo en cuenta lo que se encuentra 
disponible de manera nativa en EES. De lo evaluado, y que no se encuentra disponible en el módulo 
Heat Transfer & Fluid Flow: 
    * La función de cálculo de potencia, dada una caida de presión $\Delta P$ (*insertar cita book*).
    * etc.
* Continuar documentación en README. 