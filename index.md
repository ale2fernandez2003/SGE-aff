# SGE-aff

## ut02

### pr0201
**Pasos a realizar:**
1) Realización de un nuevo repositorio en Github.

2) Una vez creado debera vincularse a la carpeta creada con la misma estructura pedida en el ejercicio.

3) Posteriormente añadir la informacion (como estoy haciendo en este momento) de los pasos a realizar dentro del archivo ".md" desde el visual studio.

4) Una vez echo esto antes de subir los cambios a Github deberemos ir a "Settings" de nuestro resitorio e ir a "Pages" cambiando la opcion "none" por la opcion "main", para asi poder realizar una presentación del contenido mas vistoso y fluido (como en este precioso momento). 

### pr0202
**Pasos a realizar:**

1) 

## ut03
### pr0301
![Imagenes](./Imagenes/1.png)
![Imagenes](./Imagenes/2.png)
![Imagenes](./Imagenes/3.png)

**Pasos a realizar para formular una factura:**

1) Lo primero sera añadir la opcion de las Facturas a nuestro Odoo
2) Una vez ya incluida lo que tendremos que hacer es añadir una compañia nueva y darle los valores que nos piden, seran los datos de la compañia como por ejemplo el nombre de esta su dirección su email...
3) Posterior mente nos dira que modifiquemos el formato de nuestras facturas, aqui se le añadira su fondo, formato....
4) Una vez echo esto tendremos que inportar los clientes. 
5) Y por ultimo realizaremos la factura con uno de los clientes que hemos incluido anteriormente, aqui se indicara el importe a pagar del objeto, material...


### pr0302
![Imagenes](./Imagenes/5%20imagenes.png)

**Pasos a realizar para añadir fotos del inventario de Google:**

1) Lo primero sera añadir la opcion de las Productos a nuestro Odoo.

2) Luego iremos a Googles APIs y servicios y realizar un nuevo proyectopara poder obtener una nueva clave APIy una vez obtenida la nueva clave API deveremos ir a Custom Search API para ver los detalles.

3) Decpues iremos a Google Programmable Search Dashboard y crearemos un nuevo buscador, una vez creado este tendremos que darle a personalizar para obtener la IDv de buscador.

4) En Odoo iremos a Ajustes y desbloquearemos la opion de "Google Imágenes", en ella se pondran tanto la API como la ID de busqueda.

5) Y solo quedaria ir a los Productos, tendremos que insertar los valores de un archivo que nos an dado, y en la opcion de "Accion" le daremos a "Obtener imágenes de Google Imágenes" y se nos mostrara la foto que se relaciona a ese producto (no funciona con todos los productos).

### pr0303
**Pasos a realizar para conseguir una copia de seguridad en PostgreSQL:**

1) Realizaremos la copia de seguridad con el comando:
```
    pg_dump -U dbuser db_name > backup.sql
```

2)  Necesitaremos acceder a la terminal del servidor Postgres y para ello realizaremos el comando:
```
    docker-compose exec db bash
```
3) Ahora sacaremos el fichero del contenedor con el comando:
```
    docker cp contenedor:ruta_contenedor ruta_anfitrion
```

4) Despues copiar el fichero al contenedor:
```
    docker cp ruta_anfitrion contenedor:ruta_contenedor
```

5) Posteriormente crearemos la base de datos con el comando:
```
    createdb -U odoo -O odoo odoo
```

6) Y por ultimo volcaremos el contenido de la copia de seguridad con el comando:
```
    psql -U odoo odoo < backup.sql
```