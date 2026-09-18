# IntelliJ-Git-JPA-Guide

Esta es una guía para configurar un proyecto en IntelliJ IDEA con Git y crear entinties JPA (Java Persistence API) desde una base de datos. A continuación, se detallan los pasos necesarios para crear un proyecto desde cero, configurar el control de versiones con Git y establecer la persistencia de datos utilizando JPA.

## Tabla de Contenidos

- [Requisitos previos](#requisitos-previos)
- [Paso 1: Iniciar sesión en IntelliJ IDEA](#paso-1-iniciar-sesión-en-intellij-idea)
- [Paso 2: Crear un nuevo proyecto](#paso-2-crear-un-nuevo-proyecto)
- [Paso 3: Configurar GitHub en el Intellij IDEA](#paso-3-configurar-github-en-el-intellij-idea)
- [Paso 4: Subir el proyecto en GitHub](#paso-4-subir-el-proyecto-en-github)
- [Paso 5: Pushear cambios al repositorio y creación de ramas](#paso-5-pushear-cambios-al-repositorio-y-creación-de-ramas)
- [Paso 6: Crear ramas en GitHub](#paso-6-crear-ramas-en-github)
- [Paso 7: Crear entidades JPA desde la base de datos](#paso-7-crear-entidades-jpa-desde-la-base-de-datos)

---

## Requisitos previos
Antes de comenzar, asegúrate de tener instalados los siguientes componentes:
- IntelliJ IDEA (versión Community o Ultimate)
- JDK (Java Development Kit) instalado y configurado en tu sistema
- Git instalado y configurado en tu sistema
- Spring Boot (opcional, si deseas utilizarlo para tu proyecto)
- Base de datos (por ejemplo, MySQL, PostgreSQL, etc.)

## Paso 1: Iniciar sesión en IntelliJ IDEA
1. Abre IntelliJ IDEA.
2. Inicia sesión con tu cuenta de JetBrains o crea una nueva cuenta si aún no tienes una.
![imagen](images/login/intellij-login.png)
![imagen](images/login/intellij-login-1.png)
![imagen](images/login/intellij-login-2.png)
![imagen](images/login/intellij-login-3.png)

## Paso 2: Crear un nuevo proyecto
1. Haz clic en "New Project" en la pantalla de bienvenida de IntelliJ IDEA.
![imagen](images/project/project-1.png)

2. Seleccionar Springboot, poner un nombre del proyecto y marcar lo siguiente:
![imagen](images/project/project-2.png)

3. Seleccionar las dependencias necesarias para tu proyecto, como Spring Web, Spring Data JPA, y la base de datos que estés utilizando (por ejemplo, MySQL Driver).
![imagen](images/project/project-3.png)

4. Haz clic en "Create" para crear el proyecto.
![imagen](images/project/project-4.png)

## Paso 3: Configurar GitHub en el Intellij IDEA
1. Entrar a File/Settings/Version Control/Github.
![imagen](images/git/git-1.png)
![imagen](images/git/git-2.png)

2. Seleccionar si inicias sesión con token o con cuenta de Github. En este caso se inicia sesión con token. Para generar un token, ve a tu cuenta de Github, luego a Settings/Developer settings/Personal access tokens/Tokens classic y haz clic en "Generate new token". Selecciona los permisos necesarios y copia el token generado.
![imagen](images/git/git-3.png)
![imagen](images/git/git-4.png)
![imagen](images/git/git-5.png)
![imagen](images/git/git-6.png)
![imagen](images/git/git-7.png)
![imagen](images/git/git-8.png)

## Paso 4: Subir el proyecto en GitHub

1. Ir a VCS y dar click en "Share Project on GitHub". Si no aparece esta opción, asegúrate de haber configurado correctamente tu cuenta de GitHub en IntelliJ IDEA.
![imagen](images/upload/upload-1.png)

2. Ingresa el nombre del repositorio, la descripción (opcional) y desmarcar "Private" si no quieres que sea privado, y haz clic en "Share".
![imagen](images/upload/upload-2.png)

3. Una vez que el proyecto se haya subido correctamente, verás un mensaje de confirmación en la parte inferior de IntelliJ IDEA.
![imagen](images/upload/upload-3.png)

4. Para confirmar que el proyecto se ha subido correctamente, puedes ir a tu cuenta de GitHub y verificar que el repositorio se haya creado con los archivos del proyecto.
![imagen](images/upload/upload-4.png)
![imagen](images/upload/upload-5.png)

## Paso 5: Pushear cambios al repositorio y creación de ramas
1. Para realizar cambios en tu proyecto y subirlos a GitHub, primero realiza los cambios necesarios en tu código.
![imagen](images/push-branch/push-1.png)

2. Ir a la pestaña Commit y seleccionar los archivos modificados que deseas subir al repositorio. Agrega un mensaje de commit descriptivo y haz clic en "Commit and push" y luego "Commit and push anyway".
![imagen](images/push-branch/push-2.png)
![imagen](images/push-branch/push-3.png)
![imagen](images/push-branch/push-4.png)

3. Comprobar que los cambios se han subido correctamente a GitHub verificando el repositorio en tu cuenta de GitHub.
![imagen](images/push-branch/push-5.png)

## Paso 6: Crear ramas en GitHub
1. Para crear una nueva rama en tu proyecto, ve al icono de ramas en la esquina inferior derecha de IntelliJ IDEA y crea una rama, en este caso se crea la rama "dev" a partir de la rama principal.
![imagen](images/push-branch/branch-1.png)
![imagen](images/push-branch/branch-2.png)
![imagen](images/push-branch/branch-3.png)

2. Realiza cambios en la rama "dev" y súbelos a GitHub siguiendo los mismos pasos que en el Paso 5.
![imagen](images/push-branch/branch-4.png)
![imagen](images/push-branch/branch-5.png)
![imagen](images/push-branch/branch-6.png)

## Paso 7: Crear entidades JPA desde la base de datos
1. Para crear entidades JPA desde una base de datos existente, primero asegúrate de tener Mysql activado y tener una base de datos cargado. Como tenemos activado la dependencia de JPA agregado inicialmente, sino, agregar desde pom.xml.
![imagen](images/mysql/mysql-1.png)
![imagen](images/mysql/mysql-2.png)

2. Ir a Database en el panel derecho de IntelliJ IDEA y hacer clic en el icono "+" para agregar una nueva conexión a la base de datos. Selecciona el tipo de base de datos que estás utilizando (por ejemplo, MySQL) y proporciona los detalles de conexión (host, puerto, nombre de usuario, contraseña, etc.).
![imagen](images/mysql/mysql-3.png)
![imagen](images/mysql/mysql-4.png)

3. Una vez que la conexión a la base de datos esté configurada correctamente, seleccionar la base de datos.
![imagen](images/mysql/mysql-5.png)

4. Crear una carpeta llamada "entities" dentro del paquete principal de tu proyecto para almacenar las entidades JPA generadas.
![imagen](images/mysql/mysql-6.png)
![imagen](images/mysql/mysql-7.png)

5. Hacer click derecho en la base de datos y seleccionar "Create JPA Entities from Database". Esto generará las entidades JPA correspondientes a las tablas de la base de datos seleccionada.
![imagen](images/mysql/mysql-8.png)
![imagen](images/mysql/mysql-9.png)
![imagen](images/mysql/mysql-10.png)

6. Se verifica que se creó los archivos de las entidades JPA en la carpeta "entities" dentro del paquete principal del proyecto.
![imagen](images/mysql/mysql-11.png)

---

## Licencia

Este proyecto es de uso académico y educativo.