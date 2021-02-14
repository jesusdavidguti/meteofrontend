# 0 **Enunciado**

​	El tema 6 está dedicado a  DOCUMENTACIÓN Y CONTROL DE VERSIONES. Para su evaluación y calificación el alumno/a deberá elaborar y subir a Moodle un documento PDF con las capturas de pantalla y explicaciones correspondientes a las siguientes actividades:

1. Crear en GitHub 2 repositorios, uno para el backend y otro para el frontend de la aplicación desarrollada a lo largo del curso.
2. Configurar una clave SSH para acceso desde casa. Si se considera necesario puede configurarse otra clave para el acceso desde el centro educativo.
3. El uso de los comandos más frecuentes de git:

- - git clone
  - git add,  git commit
  - git log
  - git status
  - git remote

1. El uso de comandos más avanzados de git:

- - git diff, git reset, ...

1. El uso de Markdown para la documentación en el archivo README.md
2. En el trabajo deben aparecer las URLs de los repositorios en GitHub.

Se valorará:

- La estructura y orden.
- El uso de distintos tipos de formatos y recursos (imágenes, código fuente, documentación Markdown, ...)
- El nivel de detalle y de precisión en las explicaciones.

Este trabajo tiene un peso y puntúa como si se tratase de un examen.

RECURSOS:

- https://github.com/jamj2000/actividades-git
- Tutoriales y manuales disponibles en Internet

#  1 **Creación de repositorios**

​	Estos son algunos de los repositorios ya creados o "forkeados" por el usuario **jesusdavidguti**.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_5a008b29cdc7c961.png) 
 

​	Los nuevos repositorios para backend y frontend serían los siguientes: 

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_9dd50a7e3ebb4670.png) 
 

# 2 **Clave SSH**

​	Como se puede ver en el acceso desde la web, se configuró una clave SSH para acceso desde la máquina virtual de casa.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_1a23e5778d1e013a.png) 
 

​	Comprobamos en nuestra máquina virtual si, efectivamente, tenemos ya creada nuestra clave accediendo al directorio ~/.ssh

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_32547d58e4c0e60.png) 

# **3** **Uso de los comandos más frecuentes**

​	Como se puede apreciar, la parte frontend aún no ha sido clonada en local, por lo que vamos a realizar dicha operación así como algunos cambios en el código.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_69614ad38c47c7c5.png) 
 

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_2551d91d4a44dcc3.png) 
 

​	Una vez clonado, vamos a realizar algunas operaciones básicas. Aún no hemos hecho cambios de ningún tipo.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_9a980c51f611c378.png) ![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_ad86c9077db59e9e.png) 


​	Hemos creado tres nuevos ficheros con la extensión "svelte" que vamos a añadir a nuestro proyecto Github de la siguiente forma.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_45a6526fb3b7db2.jpg) 
 

​	Hemos creado también un fichero Markdown donde recogeremos este mismo documento para añadirlo al proyecto. Comprobamos el estado actual del mismo.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_e63fb4e1f6a62548.jpg) 
 

​	Comprobamos también los commits realizados.

​	![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_c8801d7d072836a9.jpg)

​	Añadimos el nuevo fichero y comprobamos el log para ver el estado actual de los cambios.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_c9795806c16971b4.jpg) 
 

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_50755a00f06f583.jpg) 


# 4 Comandos más avanzados

​	Hemos añadido unos cambios a nuestro fichero Markdown, sin embargo no queremos que dichos cambios suban por el momento.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_1c640c68f7014bae.jpg) 
 

​	Para evitar que dichos cambios suban, procedemos a "borrarlos" del control de cambios mediante un reset.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_c6452d703dc3a902.jpg) 
 

​	Procedemos a descartar dichos cambios definitivamente.

![img](file:///C:/Users/Usuario/AppData/Local/Temp/lu269620kd4j.tmp/lu269620kdnf_tmp_fe8a93543dc9829d.jpg) 
 

# 5 Uso de Markdown

​	Como se indica en el punto anterior, se ha creado un fichero Markdown (TrabajoTema6.md) que será una réplica de este mismo documento pero en formato Markdown. Para su realización vamos a utilizar el editor Typora que nos permitirá realizar dicho trabajo de una forma más rápida.

![image-20210214035535459](C:\Users\Usuario\AppData\Roaming\Typora\typora-user-images\image-20210214035535459.png)



# **6 URLs de los repositorios en GitHub**

Frontend: https://github.com/jesusdavidguti/meteofrontend.git

Backaend: https://github.com/jesusdavidguti/meteobackend.git


