# Estrategia de ramificación

## Tabla de contenido
- [Git flow](#Git-flow).
- [GitLab flow](#GitLab-flow).
- [Mainline branch](#Mainline-branch).
- [GitHub Flow](#GitHub-Flow).
- [Trunk Based Development](#Trunk-Based-Development).
- [Ship/Show/Ask](#Ship-Show-Ask).
- [Tabla estrategias de ramificación ventajas y desventajas](#Tabla-estrategias-de-ramificación-ventajas-y-desventajas).





![](https://i.postimg.cc/6QgwZsWs/estrategia1.jpg)

-  **Equipo**: habla del número de integrantes que van a afrontar el problema, el nivel de experiencia, (junior, senior).
- **Proyecto**: habla de cómo es el proyecto, si el proyecto trata de un producto, que tipo de producto.
- **Empresa**: habla de quien va enfocado, Startup; como se toman las decisiones.
- **Despliegue**: habla de cómo se hará uso del despliegue, si se sube por FTP copiando ficheros, se hace uso del despliegue continuo, con test, cobertura de código o como gustaría que fuese si existe una estrategia con menor impacto.

### Git flow
> Para más información sobre la estrategia de ramificación **GitFlow**, visitar [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/ "GitFlow")

**Git Flow** deja más organizado y seguro todo el proceso de creación de nuevos features y hotfixes dentro del código, evitando perder alguna información importante.

Es la que todo el mundo conoce por su nivel de posicionamiento en las búsquedas de internet.
![](https://i.postimg.cc/wvRN5dDD/gitFlow1.jpg)

- **Master**: se tiene una rama master que es la que está en producción.
- **Hotfix**: para trabajar en cambios imprevistos como parches para arreglar un bug o un problema en producción.
- **Release**: cuando se prepara el lanzamiento de una nueva versión, en esta estrategia cuando se tiene una nueva funcionalidad lista en develop, se realiza un release donde se probará de nuevo que todo funciona correctamente, si hay que arreglar algo; cuando la rama release esta lista, se pone en master.
- **Develop**: rama hermana de master, donde cada vez que se quiere sacar una nueva feature, se saca de Develop, cuando se termina esa característica y se ha probado se hace un merge en Develop
- **Feature(Característica)**: cuando se trabaja en una nueva característica para el proyecto, se hace una rama basada en master.

### GitLab flow
> Para más información sobre la estrategia de ramificación **GitLab Flow**, visitar [GitFlow]((https://forge.etsi.org/rep/help/workflow/gitlab_flow.md  "GitFlow")

**GitLab Flow** es una alternativa más simple a  **GitFlow**  y combina desarrollo impulsado por funciones y ramas de funciones con seguimiento de problemas. Con **GitLab Flow**, todas las funciones y correcciones van a la  rama  main mientras se habilitan   producción  y se  ramifican. GitLab Flow incluye un conjunto de mejores prácticas y pautas para garantizar que los equipos de desarrollo de software sigan un proceso fluido para enviar funciones de manera colaborativa.

![](https://i.postimg.cc/qvZSg8wg/git-Lab-Flow.jpg)

En GitLab Flow existe una rama principal que deben ser creadas al iniciar el repositorio:
 
- **Main (o master)**: Su propósito es contener el código que se encuentra en producción.
- **Develop**: Código de pre-produccion con nuevas características que todavía tienen que ser probadas y validadas pero que serán lanzadas en el próximo pase a producción.
- **PreProd(PreProduccion)**: contiene el código de producción y master realizará merge con PreProdudccion, donde se despliega y se prueban funcionalidades, con equipos móviles si se requieren.
- **Prod(Producción)**: contiene el condigo probado y verificado de PreProd.
- **Feature(Característica) o Branch**: cuando se trabaja en una nueva característica para el proyecto, se hace una rama basada en master.

### Mainline branch
> Para más información sobre la estrategia de ramificación **Mainline Branch**, visitar [Mainline Branch](https://www.bitsnbites.eu/a-stable-mainline-branching-model-for-git/ "Mainline Branch")

El modelo de línea principal estable trata de resolver el problema de las construcciones rotas. Para dar el contexto, la línea principal es la rama con la que trabajan la mayoría de los desarrolladores (a menudo llamada master en los proyectos Git), estable que está en una forma lo suficientemente buena como para que todos los desarrolladores puedan trabajar a pleno rendimiento sin ser bloqueados por las construcciones fallidas.

![](https://i.postimg.cc/DysZT3VY/Mainline-branch.jpg)

El objetivo es la simplicidad, se quita producción y pre-producción  y solo se tiene una rama master, con pocas feature(características), apenas se acabe la realización de las características se integra a master, la estrategia también habla de que antes de realizar un merge se hace una revisión de código y se practica un testing por par, donde una persona hace la funcionalidad y otro la prueba; la idea es realizar las pruebas como si fuese un usuario final.

- **Main (o master)**: Su propósito es contener el código base del cual se crearan las nuevas ramas.
- **Feature(Característica) o Branch** : cuando se trabaja en una nueva característica para el proyecto, se hace una rama basada en master.

### GitHub Flow
> Para más información sobre la estrategia de ramificación **GitHub Flow**, visitar [GitHub Flow](https://guides.github.com/introduction/flow/ "GitHub Flow")

GitHub Flow es una estrategia creada por la propia GitHub y pensada especialmente para equipos y proyectos que hacen despliegues de forma regular. Se basa en la creación de Pull Requests que serán discutidas para que se integren en la rama principal que siempre está actualizada con los cambios más recientes y preparada para ser desplegada.

![](https://i.postimg.cc/G2cYBhR2/git-Hub-flow.jpg)

- **Main (o master)**: La rama principal que contiene los cambios que se despliegan regularmente.
- Cualquier otra rama que quiere ser integrada en la rama principal.

### Trunk Based Development

> Para más información sobre la estrategia de ramificación **Trunk Based Development**, visitar [Trunk Based Development](https://trunkbaseddevelopment.com/ "Trunk Based Development")

El **Trunk Based Development ** es una estrategia que se basa en que el mayor tiempo de desarrollo se concentra en una sola rama llamada trunk (tronco) que normalmente corresponderá con main (o master). Esto quiere decir que se evita la creación de ramas auxiliares y, sólo en algunos casos que se requieran, se crean con un tiempo de vida muy limitado (máximo un par de días).

![](https://i.postimg.cc/tTXSXjmd/trunk-Based.jpg)


En esta estrategia se ***prioriza hacer commits directamente a la rama principal**. En el caso de  necesitar ramas, se hacen Pull Request pequeñas y que duren poco tiempo para ser integradas lo antes posible.

### Ship Show Ask
> Para más información sobre la estrategia de ramificación **GitHub Flow**, visitar
[Ship / Show / Ask](https://martinfowler.com/articles/ship-show-ask.html "Ship / Show / Ask")

**Ship / Show / Ask** es una estrategia de ramas que combina la idea de **crear Pull Request** con la habilidad de seguir publicando cambios rápidamente.
 
Los cambios que se crean en el repositorio se categorizan en tres:

- Ship: Se fusiona en la rama principal sin revisión.
- Show: Abre una petición de cambios para que sean revisados por CI pero se fusiona inmediatamente.
- Ask: Abre una PR para discutir los cambios antes de fusionarlos.

![](https://i.postimg.cc/9QdsVJQh/estrategia-Ship.jpg)

#### ¿Qué significa cada uno de estos nombres?

- **Ship**: Ship significa que se harán cambios directamente a la rama principal. No se esperan revisiones de código, ni integración. Vamos directos a producción (aunque antes del despliegue sí se harán los tests o checks pertinentes para evitar errores).

![](https://i.postimg.cc/VvwD7cX0/estrategia-Ship1.jpg)

------------
***Pensado para:***

- He añadido una nueva funcionalidad con un patrón establecido.
- He arreglado de forma sencilla un bug por un error.
- Actualizaciones de documentación.
- Mejora de código por feedback del equipo o la comunidad.
- Se añaden nuevos tests para evitar errores.

------------

- **Show**: En este caso sí se usa Pull Request pero no se espera revisiones manuales del código. Es decir, se **espera que los tests automatizados**, pruebas de cobertura y validación de código sean exitosos **pero no que otra persona revise el código**.

![](https://i.postimg.cc/sD4DH9CM/estrategia-show.jpg)

------------
***Pensado para:***

- Hacer arreglos necesarios para bugs y dejar constancia para que se aprenda.
- Crear pequeñas mejoras de código o refactors.
- Añadir nuevas funcionalidades siguiendo estructuras ya acordadas.
- Funcionalidades con pruebas automáticas.

------------

- **Ask**: Esta categoría es similar a Show pero aquí **sí se espera al feedback de nuestro equipo** ante de fusionar la rama. Se hace porque existe algo de incertidumbre: bien porque la solución es complicada, no sabemos implementarla, existen dudas. La idea es que la rama dure el mínimo tiempo posible para no bloquear el trabajo de otros miembros del equipo.

![](https://i.postimg.cc/sx9QJkJX/estrategia-ask.jpg)

------------
***Pensado para:***

- Cuando es un trabajo muy grande y se necesita ayuda.
- Hay dudas sobre cómo hacerlo funcionar o la calidad del código.
- Existe incertidumbre sobre lo que estamos haciendo.
- Estamos esperando a que algo ocurra para poder fusionar la rama.

------------

#### Las reglas de Ship / Show / Ask

Para poder llegar a seguir algunas de las categorías requiere algunas reglas.

1. Se tiene un buen sistema de CI/CD, fiable y rápido, que hace que la rama principal siempre sea desplegable y que evite que lleguen errores no deseados a producción.
2. Confiamos en el equipo y existen buenas prácticas de desarrollo. Pair pro gramming, mob programming, seniority, pero sobre todo existe responsabilidad. La persona se responsabiliza de decidir la categoría de su cambio. Hacer merge de tus propias Pull Request, conlleva una gran responsabilidad (no romper producción).
3. Las revisiones de código no son requerimientos para que las PR's sean fusionadas.
4. Las ramas son lo más pequeñas posibles, tienen un tiempo de vida corto y siempre salen directamente desde la rama principal.
5. El equipo ha sabido lidiar con el ego individual, confía en el resto del equipo y considera que la rama principal puede no contener código perfecto siempre y cuando las pruebas automáticas pasan.

### Tabla estrategias de ramificación ventajas y desventajas

| Estrategias de ramificación| Ventajas|Desventajas|
| :------------: | :------------: | :------------: |
| Git flow | Posee gran cantidad de documentación. | Para un equipo pequeño tener tantas ramas se vuelve muy complejo. |
| GitLab flow | Siempre se posee una rama con la cual comparar código y características. | Pull request con muchos cambios. |
| Mainline branch | Flujo de trabajo simple. |Si las ramas son largas, se acumula desarrollo en una sola rama puede generar alternancias de características. |
| GitHub Flow | Flujo de trabajo simple. |Si no se discute bien el código que se va integrar es posible afectar la funcionalidad. |
| Trunk Based Development | Facilidad de test automatizados. |La automatización debe estar implementada de forma implacable o no funcionara la colaboración en el equipo. |
| Ship / Show / Ask (Enviar, mostrar, preguntar) | Flujo de trabajo simple y rápido | Los equipos de trabajo deben tener autonomía, ser estremadamente responsables para evitar perdidas de tiempo y fallos en producción. |
