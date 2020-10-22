TERMINAL

punteros a directorios 
.. —> directorio padre
. —> directorio actual

date fecha

echo es para mostrar un mensaje en la pantalla

man man + el nombre de otro comanto, te explica todo sobre ese comando

ma + tab >> me muestra todos los comandos en el sistema que comienzan con esas dos letras

ctrl shift r busca hacia atras todos los comandos que escribi
en el hostorial cada comando tiene asignado un numero, para correrlo de nuevo
! + el numero y se re escrine el comando de mi historial

history me muestra el historial

pwd print working directory 
hostname my computer's network name 
mkdir make directory 
mkdir -p  es para hacer un path (una carpeta dentro de otra y de otra y etc)

cd change directory > es para entrar (o salir) de a directorios / carpetas
cd nombre de una carpeta, entro directo a ella ,si pongo 
cd ~ me voy a la carpeta madre. (home)
cd - me lleva a la carpeta anterior
cd .. salgo de la carpeta
cd ../../../../ salgo de todas esas carpetas 
ls list directory > this is to list what’s inside the directory ls -a  me muestra tambien los archivos ocultos
ls -l  me muestra que tipo de archivos estan visibles + usuario grupo permisos tamaño y fecha y hora de creacion
ls -la me muestra todo incluyendo archivos visibles y ocultos
ls -lh tambien miestra tamaño en Kb o Mb
ls -t  ordena los archivos por fecha de modificacion
ls -x ordena los archivos por extension
ls -r muestra el contenido de todos los directorios de forma recursiva
ls -s ordena los resultados por tamaño de archivo

rmdir + folder / directory name removes directory 
If you try to do rmdir on macOS and it refuses to remove the directory even though you are positive it's empty, then there is actually a file in there called .DS_Store. In that case, type rm -rf <dir> instead (replace <dir> with the directory name).

rm is to remove files

If you try to do rmdir on macOS and it refuses to remove the directory even though you are positive it's empty, then there is actually a file in there called .DS_Store. In that case, type rm -rf <dir> instead (replace <dir> with the directory name).

pushd push directory 
popd pop directory 

The pushd command takes your current directory and "pushes" it into a list for later, then it changes to another directory. It's like saying, "Save where I am, then go here."
The popd command takes the last directory you pushed and "pops" it off, taking you back there.
Finally, on Unix pushd, if you run it by itself with no arguments, it will switch between your current directory and the last one you pushed. It's an easy way to switch between two directories. This does not work in PowerShell.

touch crear archivos

cp copy a file or directory >> cp test.txt test2.txt >>> copia un archivo a otro
cp test.txt newdir/ >>> copia un arhivo en un directorio o carpeta
cp -r dir1 dir2 >>> copia una carpeta a otra 
The cp command will overwrite files that already exist, so be careful copying files around.

less  >> less text.txt displays the text within the file

robocopy robust copy 
mv move a file or directory >>> en realidad funciona como un rename 
si quierro mover desde el directorio anteroir al  actual:
mv ../test.txt .   >>> ese punto final refiere ami directorio atual mv test.txt ../ >>> estoy moviendo un archivo a la carpeta anterior

vim y nano permiten editar
cat es para VER el contenido entero de un archivo
head  es para ver solo las primeras lineas (seria head nombre.txt)
head -n 5  me permitiria ver las primeras 5 lineas de un archivo
tail me muestra las ultimas lineas. desde el final
tail -n 5 me muestra las ultimas 5 lineas

grep permite trabajar con expresiones regulares dentro de archivos. 
muestra las lineas que coincidan con la expresion regular que use
i.e grep palabraquebusco nombredearchivo.txt

grep -i busca la expresion sin tomar en cuenta si usa mayusculas o minusculas

si quiero buscar una frase que termine con x palabra pongo:
grep -i “palabra$” archivo.extension
grep -i “palabra’),$” archivo.extension >>> creo que es para buscar la palabra en cualquier lado no exacta

SED stream editor. puede reemplazar una expresion por ora
sed ’s/palabra/nuevepalabra/g  nombredearchivo.extension  >>> s es por select y g indica que esto se tiene que hacer globalmente, a lo largo de todo el flujo
sed ‘$d’ filename.ext elimina la ultima linea

AWK Para trabajar archivos delimitados o separados por coma, tabs, etc

ej: awk -f ‘;’ ‘{ print $1 }’ file.extensioin     >>> pongo cual es el delimitador q separa las columnas . print $1 significa q voy a imprimir solo la 1era columna
awk permite hacer calculos. ejemplo:

awk -F ‘;’ ’NR > 1 && $3 > 0 { print $1, $3 * $4 }’ file.ext

esto es… si number row mayor a y y colmna nro 3 mayor a 0, imprimir 
columna 1 y columna 3 x 4 del archivo x


more page through a file 
type print the whole file 
forfiles run a command on lots of files 

dir -r find files 

select-string find things inside files 
help read a manual page 
helpctr find what man page is appropriate 

echo print some arguments 

set export/set a new environment variable 
exit exit the shell 
runas DANGER! become super user root DANGER! 

xargs

sudo

chmod

chown


