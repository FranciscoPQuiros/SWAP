#Practica 3

* Tras la instalacion de nginx realizando el proceso indicado en la practica copio el contenido que deberia tener el archivo de configuración.
![Configurando nginx](nginx_conf.png "Configurando nginx")

* Tras guardar el archivo reiniciamos el servicio y comprobamos mediante los mensajes de salida que no hay problemas.

* Modifico el cron de la máquina 2 y modificamos los fichero hola.txt de los servidores finales, para que cuando se soliciten con curl se vean las diferencias.
![Solicitando hola.txt](curl_nginx.png "Solicitando hola.txt")

* Tambien comprobamos el balanceo mediante ponderancion añadiendo "pesos" de carga distintos a los servidores:
	weight = 2
	weight = 1

Obtenemos como respuesta a lo solicitado:
![Configurando nginx con ponderación](nginx_pon.png "Configurando nginx con ponderación")

* Realizo el mismo proceso para que funcione haproxy. Este es el contenido del archivo haproxy.conf.
![Configurando haproxy](haproxy_conf.png "Configurando haproxy")

* Tral salvar el archivo comprobamos que funciona perfectamente el balanceo.