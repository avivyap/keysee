

Estamos de vuelta con cositas frescas, como este keylogger para una vulnerabilidad XSS.


Esta herramienta sirve para que atraves de una vulnerabilidada XSS puedas obtener contraseñas, ya que el usuario las escribe y tu las lees en texto plano. Las letras que escribe la victiama ta las manda a una pagina http, que nos montamos con python3.

Este script NO se ejecuta en el terminal como un script normal, se ejecuta en la pagina web en la que hemos encontrado la vulnerabilidad XSS, asi que tienes que copiarlo y ponerlo en ese sitio.


*Importante* Cambiar la parte donde dice "ipAtacante" por tu ip 




*Cosas que hacer antes de ejecutar el script*


Tienes que ponerte en escucha por el puerto 80 con phyton3

	python3 -m http.server 80




Otra opcion que puedes usar es
	
	python3 -m http.server 80 2>&1 | grep -oP 'GET /\K.[^.*\s]+'

		- grep es para filtrar desde la palabra get en adelante

		- /\K.* esto te reseta el punto de machin y te muestra menos cosas que son inútiles

		- .*\s+ para que te filtre toda la información


Despues de eso puedes utilizar ya el script :)
		



										!!Y dentro de poquito subire una caja de herramientas para los XSS!!