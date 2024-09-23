
# SeriesTv

## Descripción

**SeriesTv** es una aplicación de escritorio desarrollada en Java que permite gestionar información sobre series de televisión. Los usuarios pueden buscar series, visualizar detalles como el título, fecha de lanzamiento, temporadas, sinopsis, género y actores, además de crear, guardar, eliminar y limpiar los datos de las series. 

El proyecto utiliza una base de datos SQL para almacenar y recuperar la información de las series.

## Características

- Búsqueda de series por código.
- Visualización de detalles de la serie (título, fecha de lanzamiento, temporadas, sinopsis, género y actores).
- Creación, actualización y eliminación de registros de series.
- Limpiar los campos de entrada para facilitar nuevas consultas o registros.
- Persistencia de datos mediante una base de datos SQL.

## Tecnologías Utilizadas

- **Java**: Lenguaje de programación utilizado para la lógica del negocio y la implementación de la interfaz gráfica.
- **Swing**: Biblioteca de Java utilizada para crear la interfaz gráfica (GUI) de la aplicación.
- **SQL**: Lenguaje de consulta utilizado para gestionar la base de datos de las series.
- **JDBC (Java Database Connectivity)**: Herramienta que permite conectar y ejecutar operaciones en la base de datos SQL desde la aplicación Java.

## Instalación

### Prerrequisitos

- **Java JDK 8 o superior**.
- Un sistema de base de datos SQL (por ejemplo: MySQL o SQL Server).
- Un IDE como **Eclipse** o **IntelliJ IDEA** para ejecutar el proyecto.

### Pasos de Instalación

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/leydytagu/seriesTV.git
   ```

2. **Configurar la base de datos**:
   
   - Crear una base de datos en tu sistema SQL. Puedes usar el nombre `series_tv_db`.
   - Ejecutar el script SQL ubicado en la carpeta `database` del proyecto para crear las tablas necesarias. Si no tienes el script, crea manualmente una tabla con la siguiente estructura:

   ```sql
   CREATE TABLE series (
       codigo INT PRIMARY KEY,
       titulo VARCHAR(255),
       fecha_lanzamiento DATE,
       temporadas INT,
       genero VARCHAR(100),
       actores TEXT,
       sinopsis TEXT
   );
   ```

3. **Configurar la conexión a la base de datos**:

   Modifica las credenciales en la clase de conexión a la base de datos (`DatabaseConnection.java` o similar). Asegúrate de que coincidan con las de tu entorno local.

   ```java
   String url = "jdbc:mysql://localhost:3306/series_tv_db";
   String user = "tu_usuario";
   String password = "tu_contraseña";
   ```

4. **Compilar y ejecutar el proyecto**:

   Abre el proyecto en tu IDE preferido, compílalo y ejecútalo.

## Uso

1. **Buscar Series**: Ingresar un código de serie en el campo correspondiente y presionar el botón "Buscar" para obtener la información almacenada en la base de datos.
2. **Crear Series**: Llenar los campos de la serie y presionar "Crear" para añadir la nueva serie a la base de datos.
3. **Guardar Cambios**: Editar los datos de una serie y hacer clic en "Guardar" para actualizar la información.
4. **Eliminar Series**: Seleccionar una serie y presionar "Eliminar" para eliminarla de la base de datos.
5. **Limpiar Campos**: Hacer clic en "Limpiar" para borrar los datos de los campos y realizar nuevas operaciones.

## Captura de Pantalla
<img width="1099" alt="Captura de pantalla 2024-09-22 a la(s) 9 25 00 p  m" src="https://github.com/user-attachments/assets/fdcd794e-ef65-4486-adc4-e557b36445e0">


## Contribuciones

Las contribuciones son bienvenidas. Para contribuir sigue estos pasos:

1. Realiza un fork del proyecto.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza los cambios necesarios y haz un commit (`git commit -m 'Agregada nueva funcionalidad'`).
4. Haz push de la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request en GitHub.

## Licencia

Este proyecto está licenciado bajo la licencia MIT. Para más detalles, consulta el archivo [LICENSE](LICENSE).
