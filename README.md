Sigue estos pasos para configurar el proyecto  en tu entorno local:

1. Clona el repositorio del proyecto:

2. Accede a la carpeta del proyecto:

3. Ejecuta el siguiente comando para iniciar los contenedores de Docker:

   ```shell
   docker-compose up -d
   ```

   Esto creará y ejecutará los contenedores de Docker necesarios para el proyecto.

4. Una vez que los contenedores estén en ejecución, ejecuta las migraciones de la base de datos:

   ```shell
   docker-compose exec web python manage.py makemigrations
   ```

   ```shell
   docker-compose exec web python manage.py migrate
   ```

   Esto aplicará las migraciones y creará las tablas necesarias en la base de datos.

6. Crea una cuenta de administrador utilizando el siguiente comando:

   ```shell
   docker-compose exec web python manage.py createsuperuser
   ```
