# PHP
## Manipular Cadenas
~~~ php
strlen("cadena"); //Devuelve la longitud de una cadena.
str_word_count("cadena"); // Cuenta palabras en una cadena.
strrev("cadena"); // Invierte una cadena.
strpos("cadena en la que buscar", "texto a buscar"); //Busca un texto dentro de una cadena y devuelve la posición donde empieza.
str_replace("texto antiguo", "texto nuevo", "cadena en la que buscar"); //Reemplaza texto dentro de una cadena .
~~~
## Manipular Num
Un alias significa que se comporta igual que.
~~~ php
is_int();
is_integer(); // - alias de is_int()
is_long(); //- alias de is_int()
is_float();
is_doble(); //- alias de is_float()
~~~
### var_dump()
~~~
La función var_dump() imprime por pantalla el tipo y el valor de una variable, y podemos utilizarla para obtener información sobre ella. 
~~~
### Otros:
~~~php
echo (pi()); // Pi:
// Min y Max
echo(min(0, 150, 30, 20, -8, -200)); // ->> -200
echo(max(0, 150, 30, 20, -8, -200)); // ->> 150
// Raiz cuadrada
echo(sqrt(64)); // ->> 8
// Redondea conmedio de (0,50)
echo(round(2.60)); // ->> 3
echo(round(1.49)); // ->> 1
// Numero aleatorio
echo(rand()); // Num aleatorio sin limitar
echo(rand(1, 10)); // Num de 1 a 10
~~~
## Constante
~~~php
// Name constante, dato constante.
define("CAPITAL","Madrid");
define ("NUMERO_PAGAS", 14);
define ("MASA_ELECTRON", 9.109E-31);
~~~

# Operadores y lectura de datos en PHP
- El código PHP va dentro de un fichero HTML, y por tanto debe ir escrito dentro de una etiqueta especial que le indique al servidor web que ahí dentro hay código PHP
~~~html
<html>
<head></head>
    <body>
        <h2>
            <?php echo "Hola mundo"?>
        </h2>
    </body>
</html>
~~~
## Var:
~~~php
<?php
$saludo = "Mundo";
$edad = 9;
echo "Hola ".$saludo." qué tal?"; // los Puntos para la Variable
print "La variable \$edad contiene el valor:".$edad;
?>
~~~
### PHP soporta los siguientes tipos de datos:
1. String
2. Integer
3. Float (números decimales "coma flotante")
4. Boolean
5. Array
6. Object
7. NULL
8. Resource
# Operadores en PHP
|Operador|Operación|Ejemplo|Se evalúa como…|Observaciones|
|:-:|:-|:-:|:-:|-|
|\*\*|Exponente (Potencia)|2\*\*3|8|Equivale a 23 que equivale a 2\*2\*2|
| % | Módulo (resto de la división entera) | 22%8 | 1 | 22/8 da 2, y de resto da 6 |
| / | División|22/8 | 2,75 |
| * | Producto|3*5 | 15 |
| - | Resta | 5-2 | 3 |
| + | Suma | 2+ 2| 4 |
### Operadores de asignación 

|Asignación|Equivale a|Explicación|
|:-:|:-:|:-|
|x = y|x = y|El operando izquierdo almacena el valor de la expresión de la derecha|
|x += y | x = x + y | Sumo x e y, y el resultado lo almaceno en x|
|x -= y | x = x - y | Resto x e y, y el resultado lo almaceno en x|
|x *= y | x = x * y | Multiplico x e y, y el resultado lo almaceno en x|
|x /= y | x = x / y | Divido x e y, y el resultado lo almaceno en x|
|x %= y | x = x % y | Calculo el resto de x/y, y lo almaceno en x|

### Operadores de comparación
|Operador |Nombre |Traducción |Ejemplo |Resultado|
|:-:|-|-|:-:|:-|
|==| Equal| Igual| $x == $y| Devuelve verdadero si $x es igual a $y|
|===| Identical| Idéntico| $x === $y| Devuelve verdadero si $x es igual a $y, y son del mismo tipo.|
|!= ó <>| Not equal| No es igual| $x != $y ó $x <> $y| Devuelve verdadero si $x no es igual a $y|
|!==| Not identical| No es idéntico| $x !== $y| Devuelve verdadero si $x no es igual a $y, o si no son del mismo tipo|
| > | Greater than| Más grande que| $x > $y| Devuelve verdadero si $x es mayor que $y|
| < | Less than| Menos de| $x < $y| Devuelve verdadero si $x es menos de $y|
| >= |Greater than equal to|Mayor o igual que| $x >= $y| Devuelve verdadero si $x es mayor o igual a $y|
| <= |Less than or equal to| Menor o igual que |$x <= $y |Devuelve verdadero si $x es menos o igual a $y1
|<=> |Spaceship| Nave espacial |$x <=> $y| Devuelve -1, 0 ó 1, dependiendo de si $x es menor, igual o mayor que $y. A partir de PHP 7|

### El operador == (igual a) consta de dos caracteres, como también lo hace el operador != (no igual a)
|Operador |Nombre |Traducción |Resultado|
|:-:|-|-|-|
|\++$x|Pre-increment |Pre-incremento |Incrementa $x en uno, luego devuelve $x|
|$x++|Post-increment |Post-incremento |Devuelve $x, luego incrementa $x en uno|
|\--$x|Pre-decrement |Pre-decremento |Disminuye $x en uno, luego devuelve $x |
|$x--|Post-decrement |Post-decremento |Devuelve $x, luego disminuye $x en uno|
## Operadores Booleanos
Existen tres operadores Booleanos, que se usan para comparar valores Booleanos, que son `and(&&)`, `or(||)`, `xor(xor)` y `not(!)`.

### AND o && (Y)
|Expreción|Evalua como|
|-|-|
|False `&&` False | False|
|False `&&` True | False|
|True `&&` False | False|
|True `&&` True | True|
### OR o || (O)
|Expreción|Evalua como|
|-|-|
|False `\|\|` False | False|
|False `\|\|` True | True|
|True `\|\|` False | True|
|True `\|\|` True | True|
### XOR (O exclusiva)
|Expreción|Evalua como|
|-|-|
|False `XOR` False | False|
|False `XOR` True | True|
|True `XOR` False | True|
|True `XOR` True | False|
### NOT (NO)
|Expreción|Evalua como|
|-|-|
|`!True` | False|
|`!False` | True|
### Operadores de cadenas
|Operador |Nombre |Traducción |Ejemplo |Resultado|
|-|-|-|-|-|
|`.` |Concatenation |Concatenación |``$txt1 . $txt2``| Devuelve el contenido de $txt1 seguido de $txt2|
|`.=` |Concatenation assignment |Asignación de concatenación|``$txt1 .= $txt2``| Almacena en $txt1 el resultado de concatenar $txt1 y $txt2 |
## Lectura de datos desde teclado. Formularios HTML 
Los datos del formulario se envia en metodo POST:`methop='POST'`
~~~html
<form action='submit.php' methop='POST'>
Introduce el valor: <input type="text" name='Valor'></br>
<input type="submit">
</form>
~~~
Ahora para guardar el valor en una variable en el PHP: `$_POST['var']`
~~~php
$Valor = $_POST['Valor'];
echo $Valor; // Nos sale el valor
~~~
# Control de flujo Introducción
~~~mermaid
graph LR
    A[Inicio] --> B{Esta lloviendo?}
    B -->|si| C{Tienes Paraguas?}
    B -->|NO| P[Sal a la calle?]
    C -->|SI| P
    B -->|NO| E[Espera un poco]
    E --> R[Esta lloviendo?]
    R -->|SI| E
    R -->|NO| P
    P --> y[Fin]
~~~
## IF
~~~php
$nota = 4;
if ($nota < 5) {
    echo "Suspenso! "; // Si la condicion es True se ejecuta el codigo.
}
~~~
## IF ELSE
~~~php
$nota = 5;
    if ($nota <= 4.99) {
        echo "Suspenso! " ; // Si la nota es Menor o igual a 4.99 se ejecuta el CODE.
    } else {
        echo "Aprobado" ; // <-- SI NO SE EJECUTA ESTO.
    }
~~~
## ELSEIF
~~~php
$hora = 11;
    if ($hora < 7) { // <-- si no se cumple esto pasa al siguente
    echo "5 minutos más...";
    }elseif($hora < 12){ // <-- si no se cumple esto pasa al siguente
        echo "Buenos días";
    }elseif($hora < 20) { // <-- si no se cumple esto pasa al siguente
        echo "Buenas tardes "
    }else{ // <-- Termina con esto por No tener otra Opc
        echo "Buenas noches ";
    }
~~~
## SWITCH
~~~php
$moneda = "cara";
switch ($moneda) {
    case "cara":
        echo "Ha salido cara";
        break;
    case
        echo "Ha salido cruz"
        break;
    default:
        echo "no ha salido ni cara ni cruz";
}
~~~
***
# Bucles
## WHILE
~~~php
$contador = 1;
    while($contador <= 5) { // Solo va a parar cuando la variable sea <= que 5
        echo "La variable \$contador vale:$contador <br>";
        $contador++;
    }
    echo "Se ha terminado el bucle";
~~~
## DO .. WHILE
~~~php
$x = 1;
    do{
        echo "La variable \$x vale:$x <br>";
        $x++;
    }while($x <= 5)
~~~
## FOR
~~~php
for ($x = 0;$x <= 10; $x++){
    echo "El contador vale: $x </br>" ;
}
~~~
# Formularios
## Acceso a formularios desde PHP
~~~html
<!-- Fichero 1.php -->
<HTML>
<BODY>
    <FORM ACTION=”2.php” METHOD=”POST”>
        Edad: <INPUT TYPE=”text” NAME=”edad”>
        <INPUT TYPE=”submit” VALUE=”aceptar”>
    </FORM>
</BODY>
</HTML>
~~~
~~~php
// Fichero 2.php
$edad = $_POST['edad'];
print (“La edad es: $edad”);
~~~
## Elementos de tipo INPUT
### TEXT
~~~html
<!-- HTML -->
Introduzca la cadena a buscar:
<INPUT TYPE="text" NAME="cadena" VALUE="valor por defecto" SIZE="20">
~~~
~~~php
// PHP
<?PHP
    $cadena = $_POST[‘cadena’];
    print ($cadena);
?>
~~~
### Radio
~~~html
<!-- HTML -->
Sexo:
<INPUT TYPE="radio" NAME=“sexo" VALUE=“M“ CHECKED>Mujer
<INPUT TYPE="radio" NAME=“sexo" VALUE=“H">Hombre
~~~
~~~php
// PHP
<?PHP
    $sexo = $_POST[‘sexo’];
    print ($sexo);
?>
~~~
### CHECKBOX
~~~html
<!-- HTML -->
<INPUT TYPE="checkbox" NAME="extras[]" VALUE="garaje" CHECKED>Garaje
<INPUT TYPE="checkbox" NAME="extras[]" VALUE="piscina">Piscina
<INPUT TYPE="checkbox" NAME="extras[]" VALUE="jardin">Jardín
~~~
~~~php
// PHP
<?PHP
    $extras = $_POST[‘extras’];

    foreach ($extras as $extra)
        print (“$extra <BR>\n”);
?>
~~~
### BUTTON
~~~html
<!-- HTML -->
    <INPUT TYPE="button" NAME=“actualizar" VALUE="Actualizar datos">
~~~
~~~php
// PHP
<?PHP
    $actualizar = $_POST[‘actualizar’];
    
    if ($actualizar)
        print ("Se han actualizado los datos");
?>
~~~
### PASSWORD
~~~html
<!-- HTML -->
    Contraseña: <INPUT TYPE="password" NAME="clave">
~~~
~~~php
// PHP
<?PHP
    $clave = $_POST[‘clave’];
    print ($clave);
?>
~~~
### SUBMIT
~~~html
<!-- HTML -->
    <INPUT TYPE="submit" NAME="enviar" VALUE="Enviar datos">
~~~
~~~php
// PHP
<?PHP
    $enviar = $_POST[‘enviar’];

    if ($enviar){
        print ("Se ha pulsado el botón de enviar");
    }
?>
~~~
### SELECT Simples
~~~html
<!-- HTML -->
Color:
<SELECT NAME=“color">
    <OPTION VALUE=“rojo" SELECTED>Rojo
    <OPTION VALUE=“verde">Verde
    <OPTION VALUE=“azul">Azul
</SELECT>
~~~
~~~php
// PHP
<?PHP
    $color = $_POST[‘color’];
    print ($color);
?>
~~~
### SELECT Múltiple
~~~html
<!-- HTML -->
Idiomas:
<SELECT MULTIPLE SIZE="3" NAME="idiomas[]">
    <OPTION VALUE="ingles" SELECTED>Inglés
    <OPTION VALUE="frances">Francés
    <OPTION VALUE="aleman">Alemán
    <OPTION VALUE="holandes">Holandés
</SELECT>

~~~
~~~php
// PHP
<?PHP
    $idiomas = $_POST[‘idiomas’];

    foreach ($idiomas as $idioma)
        print (“$idioma <BR> \n”);
?>
~~~
### TEXTAREA
~~~html
<!-- HTML -->
Comentario:
<TEXTAREA COLS=“50" ROWS=“4" NAME="comentario">
    Este libro me parece ...
</TEXTAREA>
~~~
~~~php
// PHP
<?PHP
    $comentario = $_REQUEST[‘comentario’];
    print ($comentario);
?>
~~~
***
## ISSET
~~~php
<?php
    if(isset($_POST['enviar'])){ 
            // code
        }else{
?>
        // code HTML
<?php
}?>
~~~
***
# Funcion
~~~php
function sumar ($a1, $a2) {
    return $a1 + $a2;
}
    $s = sumar (2, 4); //Se llamam la Funcion y se pasa los valores por parámetro
    echo "La suma es: $s";
~~~
# ARRAYS
