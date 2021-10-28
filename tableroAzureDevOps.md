# Configuración del tablero en Azure DevOps

## Tabla de contenido
- [Creación de tareas](#Creación-de-tareas).

## Documentaciones

- **Documentación estrategias de ramificación:** [Estrategia de ramificacion](https://github.com/escobarjsa/azureDevOps/blob/main/README.md)
- **Documentación del tablero de Azure DevOps:** [Tablero Azure DevOps](https://github.com/escobarjsa/Estrategias-de-ramificacion-Branching-/blob/main/tableroAzureDevOps.md)
- **Documentación de Azure DevOps:** [Azure DevOps](https://github.com/escobarjsa/azureDevOps/blob/main/Azure%20DevOps.md)

### Creación de tareas

Para la creación de un Sprint, es necesario dirigirse a Boards, después a Sprints.

![](https://i.postimg.cc/sDKg2DRf/1-inicio.jpg)

En la opción de Sprints, damos en **New** y ahí nos desplegará una ventana para la configuración del nuevo Sprint, donde pedirá nombre, la fecha de inicio y la fecha de fin, además de ello asociado a que equipo de trabajo.

![](https://i.postimg.cc/J0xMtKvY/1.jpg)

Después de crear el Sprint, hay que ir a configuraciones y mirar el tipo de tareas que se crearan, si son de tipo **Epics**, **Features** y **Stories**, para efectos prácticos de este ejemplo se seleccionan los tres.

![](https://i.postimg.cc/024hnLYd/3.jpg)

Para crear las tareas, se selecciona en **"New Work Item"**, y se procede a asignar un nombre asociado a lo que se requiere.

![](https://i.postimg.cc/tgpkN5MN/4.jpg)

Una vez creado damos en el signo más, para agregar una **Feature**.

![](https://i.postimg.cc/BnGkR2zX/5.jpg)

Para agregar una nueva **Feature**, se le asigna un nombre, una descripción, además en el apartado de **planning** agregar el nivel de riesgo y guardar los cambios.

![](https://i.postimg.cc/Df9MbqnB/6.jpg)

Para crear una historia se debe asignar el nombre, el nivel de riesgo y posteriormente guardar los cambios.

![](https://i.postimg.cc/Fz3GxBNG/7.jpg)

Para crear una tarea o un bug, se procede a oprimir en el más y elegir lo que se requiere.

![](https://i.postimg.cc/brc9d9kn/8.jpg)

Para la creación de una tarea se debe elegir el nombre, en el apartado de **Effort (Hours)**, definir la cantidad de horas estimadas, también recordar poner el número de horas completadas al finalizar la tarea o si no se finalizó el número de horas gastadas y las que falta.

![](https://i.postimg.cc/k48xrRzg/9.jpg)

Una vez tenemos las tareas definidas, nos dirigimos a **Boards**, para ver el tablero, las tareas nuevas, activas, resueltas y las que están cerradas.

![](https://i.postimg.cc/76v2NYh8/10.jpg)

En **"Work items"**, se puede ver la clasificación de los elementos de trabajo.

![](https://i.postimg.cc/pX056BrB/11.jpg)

Una vez se tienen las tareas asignadas, se procede a subir cambios y realizar un **Pull Request**, se asigna la tarea que se está integrando, en el apartado de **Work items to link**, se selecciona la tarea para proceder a crear el **Pull Request.**
![](https://i.postimg.cc/hP7RkDP3/12.jpg)

Por último, una vez creado el Pull Request, se puede visualizar en **"Work items"**, la tarea que se hace referencia el respectivo** Pull Request**, este apartado se discutirá lo que se va  a integrar para proceder a su aprobación.

![](https://i.postimg.cc/66Fp218g/13.jpg)
