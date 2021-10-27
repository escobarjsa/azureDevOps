# Azure DevOps

## Tabla de contenido
- [Configuración de ramas en Azure DevOps](#Configuración-de-ramas-en-Azure-DevOps).
- [Configuración Pipelines](#Configuración-Pipelines).


### Configuración de ramas en Azure DevOps

Cuando se inicia un nuevo repositorio, ya teniendo el proyecto base, hay que realizar unas configuraciones básicas para, la primera es estando en "Repos", dirigirse a "Branches".

![](https://i.postimg.cc/1tzdyV8p/1.png)

Ya en "Branches", se selecciona los tres puntos para abrir el menú desplegable, se selecciona "Branch policies".

![](https://i.postimg.cc/pX8Rw3bP/2.jpg)

En Branch policies, activamos "Require a minimum number of reviewers", ahí pide un número mínimo de personas que revisaran código, para efectos prácticos se eligieron dos personas, pero esto varia del tamaño del equipo, además si se requieren activar otras opciones depende del enfoque dado.

![](https://i.postimg.cc/sf4JTg1z/3.jpg)

Además si ya se tiene un Pipeline configurado se puede agregar al apartado de compilación para que el proyecto corra cada vez que tenga nuevas funcionalidades.

![](https://i.postimg.cc/hvc6NZ9t/4-1.jpg)

### Configuración Pipelines

Para la configuración de los Pipelines es necesario dirigirse al apartado de Pipelines, ahí se selecciona "New" para crear un nuevo Pipelines.

![](https://i.postimg.cc/25B55ygB/22.jpg)

Cuando se selecciona la opción de new, se despliegan un conjunto de opciones, para tomar un código como referencia, desde diferentes plataformas, para este caso se seleccionara "Use the classic editor".

![](https://i.postimg.cc/NfMBMLHf/5.jpg)

En este apartado seleccionamos el origen de nuestro código, el equipo, el repositorio, la rama a la cual va a ir enfocado el pipeline, ya estando seguros damos "Continue".

![](https://i.postimg.cc/G22qY0JY/6.jpg)

Azure DevOps, tiene pre definido algunas configuraciones, para efectos prácticos se seleccionó "Select a template", el cual es un archivo YAML en blanco.

![](https://i.postimg.cc/02pF9st2/7.jpg)

En este apartado se tiene el nombre del Pipeline, la especificación de donde se va a compilar el proyecto, el número de trabajos.

![](https://i.postimg.cc/9Fjg8kW3/8.jpg)

Para agregar un trabajo damos en el más señalado en la imagen, después se pueden buscar las tareas que se necesitan al aparatado derecho "Add tasks".

![](https://i.postimg.cc/0yXfsXqy/9.jpg)

La primer tarea que se selecciona para este ejemplo es una tarea de "Restore", en Command se puede seleccionar el tipo de tarea.

![](https://i.postimg.cc/wjrhPtht/10.jpg)

Además se agregara una tarea de Build, por último se agrega una tarea de Artifact, para la creación de un artefacto.

![](https://i.postimg.cc/pXXzLQCh/13.jpg)

Si se requiere ver el código YAML que se está implementando, en el apartado de "View YAML".

![](https://i.postimg.cc/hjB7WVhG/14.jpg)

Una vez ya tenemos las tareas definidas, se procede a ir al apartado "Save & Queue".

![](https://i.postimg.cc/jjQSfmds/15.jpg)

Por ultimo nos muestra un resumen de las tareas, un comentario si se quiere poner, la máquina que va a correr el Pipeline y la rama.

![](https://i.postimg.cc/7hpkdnYs/16.jpg)

En este apartado ya se está ejecutando la tarea.

![](https://i.postimg.cc/Jh1WfnML/18.jpg)

Se previsualiza la ejecución de las tareas ya previamente configuradas y la visualización  del artefacto.

![](https://i.postimg.cc/jSRxbv4m/20.jpg)

Por último se puede visualizar el artefacto generado.
![](https://i.postimg.cc/G3YdT6M6/21.jpg)
