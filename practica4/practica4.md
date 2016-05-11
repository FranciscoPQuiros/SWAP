#Práctica 4
- Francisco Alfonso Peña Quiros

##-Pruebas con ApacheBenchmark

* Debemos realizar las pruebas a 1 servidor y con balanceo de carga con la siguiente orden de comandos
**ab -n 1000 -c 5 http://ip_maquina.com/prueba.html**.

* Mostramos las siguientes imágenes con las pruebas de rendimientos en los 3 casos.

	![Pruebas con nginx](ab-balanceo.png "Pruebas coan nginx")

	![Pruebas con haproxy](ab-haproxy.png "Pruebas con haproxy")

	![Pruebas con 1-server](ab-m1.png "Pruebas con 1-server")

* Tras las series de pruebas, realizamos las medias de los tiempos obtenidos y mostramos las gráficas resultantes. Las dispersiones se encuentran en el **.xml**.

	![Time taken for tests](time-taken.png "Time taken for tests")

	![Requests per second](requests.png "Elapsed time")

Tambien hay que decir que el valor **Failed requests** es de 0 en todas las pruebas, por eso no muestro imagen de ello.

##-Pruebas con Siege

* Para Siege, del mismo modo que con ApacheBenchmark, usamos la siguiente linea de comandos:
**./siege -b -t60S -v http://ip_maquina.com/prueba.html**

* Ahora muestro algunas de las imágenes obtenidas tras las pruebas.

	![Pruebas con nginx](siege.png "Pruebas con nginx")

	![Pruebas con haproxy](siege-haproxy.png "Pruebas con haproxy")

	![Pruebas con 1-server](siege-m1.png "Pruebas con 1-server")

* Y ahora muestro las gráficas conseguidas, de las métricas más importantes,  por las series de pruebas realizadas con Siege.

	![Availability](availability.png "Availability")

	![Elapsed time](elapsed.png "Elapsed time")

	![Response time](response.png "Response time")

	![Transaction rate](transaction.png "Transaction rate")
