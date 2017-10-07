# Estación Meteorologica (Taller-de-proyecto-2- UNLP)
Se subiran los archivos de la Estacion Meteorologica construida para taller de proyecto 2. La misma consta de un desarrollo de Python, el cual simula a partir de distintos Threds y numeros aleatorios aproximados a la realidad. Ademas, se tubo en cuenta el uso de la base de datos de PostgreSQL. 


# Instrucciones de uso Postgres

1) Abir una terminal y colocar los siguientes comandos:

		sudo apt-get update
		sudo apt-get install postgresql postgresql-contrib
		pip install psycopg2 // si falla, buscar como instalar psycopg	

Luego se debe configurar dicho software, realizando lo siguiente:

		sudo -u postgres psql postgres

El resultado del comando anteriro, abrira la consola de postgres con el usurio "postgres".
Finalmente, tienen que seguir la siguiente secuencia:
		
		ATENCIÓN: NO DEJAR VACIO EL CAMPO DE CONTRASEÑA

		postgres=# \password postgres 
		Enter new password: 
		Enter it again: 
		postgres=# \q



2) Instalamos la interfaz para manejar Postgres:

		sudo apt-get install pgadmin3

Al inicializarla, se observaraque no se encuentra conectada la base de datos. Realizar un click izquierdo sobre "add conection to a server".

Completar de la siguiente manera:

		name: tallerDeProyecto2
		Host:localhost
		Port:5432
		Service:(vacio)
		MainenanceDB : postgres
		UserName : postgres
		passward : (la que gusten, pero la que ponga, fijense de entrar al .py y ponerle esta misma).
		
Presionar aceptar al finalizar y se tendrá el servidor creado. Paso seguido, habrá que crear la base de datos. Para esto, se debe acceder al servidor hasta que visualicen "Databases",luego realizar click derecho y crear una base de datos nueva con el nombre “practica1”. 

Si todo lo anterior se ejecutó con éxito, dentro del repositorio hay un backup con la base de datos ya iniciada. Para usarla, se debe realizar click derecho en la base de datos con el nombre practica1 ->restore... y se debe buscar la dirección en donde se encuentra dicho backup. En caso de errores en la ejecución no hay problemas, lo más probable es que sean de registros o algo en relación a la distribución de Sistema operativo donde se ejecute.


 Para poder seguir utilizando todo, sigan este tutorial:

		http://www.postgresqltutorial.com/postgresql-python/	


