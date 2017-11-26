# Q&A

* ¿Qué comando utilizaste en el paso 11? ¿Por qué?

> **git reset - -hard HEAD~1**: Utilizo este comando ya que con él retrocedo al commit padre (es decir, deshago el commit anterior moviendo los punteros HEAD y "styled" al commit padre), y con el modificador - -hard altero el contenido de mi working copy, dejándolo igual que lo que haya en el repositorio del commit al que nos movemos.


* ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

> **git reflog**: para buscar el hash SHA del commit que queremos recuperar.

> **git reset - -hard "hash SHA"**: para mover los punteros HEAD y master a dicho commit.


* El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

> No hubo conflicto, dado que tampoco hubo merge. La rama "styled" ya tenía acceso a todos los commits de la rama master, dado a que fue creada en el primer commit (donde se encuentra la rama master actualmente) y tras crearla no hicimos otro commit en la rama master.


* El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

> Sí. Hubo conflicto al *mergear* el archivo git-nuestro.md, ya que en las dos ramas se habían modificado datos en las mismas líneas. Ya que Git no desea alterar nuestro trabajo, nos avisa de que hay un conflicto y nos deja elegir con que versión quedarnos (o combinar ambas versiónes).


* El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

> No hubo conflicto, ya que los cambios que estamos asimilando de la rama "styled" (aunque tenían cambios en las mismas líneas) no tenían que eliminar ningún carácter del archivo, sólo añadir.


* ¿Qué comando o comandos utilizaste en el paso 25?

> **git log - -graph**. También podría haber utilizado el comando **git graph**, que es un alias que contiene los comandos **git log - -graph - -decorated - -pretty=oneline**.


* El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

> Sí, porqué las ramas forman una lista. Es decir que no hay ninguna ramificación, los commits están alineados y nos bastaría con mover el puntero "master" al commit donde se encuentra el puntero "title" para tener acceso a todos los commits.


* ¿Qué comando o comandos utilizaste en el paso 27?

> **git reset HEAD~1**


* ¿Qué comando o comandos utilizaste en el paso 28?

> **git checkout - -git-nuestro.md**


* ¿Qué comando o comandos utilizaste en el paso 29?

> **git branch -D title**


* ¿Qué comando o comandos utilizaste en el paso 30?

> **git reflog** : para encontrar el "hash SHA" del commit del merge.

> **git reset - -hard "hash SHA"** : para mover el puntero HEAD y master al commit del merge y así recuperar los archivos en nuestro working copy.


* ¿Qué comando o comandos usaste en el paso 32?

> **git log** : para encontrar el "hash SHA" del primer commit

> **git reset - -hard "hash SHA"** : para mover la rama "master" juntamente con el puntero HEAD al primer commmit y dejar el working copy como lo teníamos al principio (si no quisiesemos alterar el working copy podríamos usar **git reset "hash SHA"** o también podríamos movernos en *detached HEAD state* con el comando **git checkout "hash SHA"**, ya que no se indica si nos tenemos que mover con la rama).


* ¿Qué comando o comandos usaste en el punto 33?

> **git reflog** : para encontrar el "hash SHA" del último commit.

> **git reset - -hard "hash SHA"** : para movernos al último commit y dejar el working copy como lo teníamos en repositorio del último commmit.



