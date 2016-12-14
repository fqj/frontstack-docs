# Flujo de trabajo con git-flow

## Metodología
La forma en la que vamos a trabajar se basa en la metodología `git-flow, modelo propuesto originalmente por Vincent Driessen ([A successfull Git branching model](http://nvie.com/git-model))


En resumen el modelo basa en la existencia permamente de dos ramas:

- *`master`*: rama donde van a residir las versiones estables del producto, serán las que se liberen a producción. En principio cada commit de esta rama deberá llevar su tag correspondiente de número de versión. **SOBRE ESTA RAMA NO SE DEBE HACER UN COMMIT DIRECTO NUNCA**, solo debe recibir merges desde ramas inferiores.

- *`develop`*: rama de desarrollo, aquí residirá todo el código que se va generando mergeado desde las ramas features, **al igual que master sobre esta rama no se debe hacer un commit directo nunca**.

Además de estas dos ramas, también tendremos ramas temporales:

- *`feature/nombre_rama_feature`*: Son ramas que deberán contener el bloque de una funcionalidad específica. Se deben crear a partir de la rama *develop* y morir al integrarse de vuelta en la misma.

- *`hotfix/nombre_rama_hotfix`*: Se crean a partir de la rama master. Son ramas inmediatas que se crean para solucionar bugs críticos en el código ya liberado. 
  Al terminar se integran de vuelta a *master* directamente y se hacen descender los cambios también hacia *develop* para incorporar
  el nuevo código al desarrollo en proceso. *La única excepción de esta regla es que cuando exista rama release los cambios deben mergearse hacia release y no hacia develop*. Una vez completado el ciclo la rama muere o queda
  congelada, por lo que si en el futuro es necesario integrar otro grupo de fixes será necesario crear otra rama hotfix.

- *`release/nombre_rama_release`*: Cuando se quiere liberar una nueva versión del producto, se crea una rama release candidate directamente desde *develop*. 
  Una vez creada esta rama sobre ella no se incorpora ninguna funcionalidad nueva siendo cada commit orientado expresamente a la 
  solución de errores para su estabilización y lanzamiento a *master*. Una vez estabilizada y pasados los tests correspondientes se mergean los cambios hacia 
  *master* y se taggea con una nueva versión. Luego se mergean de vuelta a *develop* para integrar los fixes creados y se congela o muere la rama release.


## Ejemplo de uso
Ahora, se va a explicar cual podría ser el flujo de trabajo para la siguiente situación: tenemos una versión estable en master (v_1.0). A su vez, tenemos que llevar a cabo dos desarrollos independientes. Además, nos vamos a dar cuenta que tenemos un bug reconocido (bug1), y nos han abierto una issue (issue_1). En el caso de la issue, será necesario que salga en la versión liberada en cuanto esté solucionado.

1. Desde la rama develop vamos a crear dos ramas de feature (feature/f1 y feature/f2).
2. En cada una de las ramas de feature se van a desarrollar las funcionalidades solicitadas.
3. Cuando nos damos cuenta de que tenemos el bug1 en producción, pero este bug no es necesario liberarlo en la versión estable, lo que hacemos es solucionar el bug en la rama develop. En caso de que el bug sea lo suficientemente complejo como para tener que desarrollarlo a parte de la rama develop, nos vamos a poder crear una rama feature/solucion_bug1 donde se solucionaría el bug y, posteriormente, se hará un merge a la rama develop.
4. En el momento en el que nos abren la issue_1 lo que haremos será sacar una rama de issue desde master (issue_1). Tras solucionar este problema haremos un merge de la solución tanto en máster como en develop, para así tener la solución tanto en la rama estable como en la rama de develop. Crearemos un tag en máster con la nueva versión de la herramienta.
5. A medida que vayamos terminando de desarrollar cada feature iremos haciendo un merge a la rama develop con todos los cambios.
6. Una vez que ya se han terminado todas las features y se han hecho todos los merges a develop vamos a proceder a hacer el merge a la rama master y crear el tag de version, para así tener disponible nuestra nueva versión estable de la herramienta liberada.

## Descarga de git-flow
Para poder tener acceso a git flow desde la consola de comandos de windows será necesario realizar los siguientes pasos:
1. Descargar los binarios de: [http://gnuwin32.sourceforge.net/packages/util-linux-ng.htm](http://gnuwin32.sourceforge.net/packages/util-linux-ng.htm)
2. Descomprimir el fichero descargado.
3. Copiar getopt.exe en la ruta "C:\Program Files (x86)\Git\bin"
4. Clonar el repositorio de git-flow donde quieras: git clone –recursive https://github.com/nvie/gitflow.git
5. Ir al repositorio clonado y en "cd contrib/" ejecutar: 
    "msysgit-install.cmd "C:\Program Files (x86)\Git"
6. Ya está instalado. Si ejecutas "git flow" en una consola ya te lo reconoce.

_Fuente:_ [http://aprendegit.com/instalacion-de-git-flow/](http://aprendegit.com/instalacion-de-git-flow/)

## Comandos de creación y finalización de features y hotfixes
Algunos comandos para la creación y finalización de features y hotfixes:
- Features:
    - git flow feature start nombre_de_feature: Al iniciar una funcionalidad. Nos crear la rama y nos pone en ella.
    - git flow feature finish nombre_de_feature: Ya hemos hecho todos los commit en la feature y hemos terminado el desarrollo. Con este comando nos fusiona la rama con develop, borra la rama y cambiamos a develop.
    - git flow feature checkout nombre_de_feature: Volver a la rama de una feature para seguir desarrollando en ella.
- HotFix:
    - git flow hotfix start nombre_hotfix: Se crea la rama a partir de master para comenzar a desarrollar el hotfix.
    - git flow hotfix finish nombre_hotfix: Se ha terminado de solucionar el error. Esto fusiona los cambios tanto a develop como a master.

