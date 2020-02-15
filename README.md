# KeepcodingPracticaGit
Práctica del curso de git, gitHub y Sourcetree

1 - ¿Qué comando utilizaste en el paso 11? ¿Por qué?

>> git reset --hard HEAD~1

Porque reset me permite modificar a donde apunta mi HEAD, --hard elimina las modificaciones en el working copy y HEAD~1 apunta al commit anterior.


2 - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

>> git reflog

Para buscar todo el trabajo que he realizado en el proyecto hasta ahora.
Busqué el commit que incluía las modificaciones del archivo git-nuestro.md.

>> git reset --hard 6c1d202

Para que mi HEAD apunte a ese commit con --hard para traerme los cambios al working copy.


3 - El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

El resultado fue un "Already up to date" dado que master no sufrió ningún cambio desde que se creó la rama Styled, de modo que no tenía nada que actualizar. Solo la rama styled sufrió modificaciones.


4 - El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

Sí que causó un conflicto. Porque en la rama htmlify se modificaron las mismas partes del archivo que se modificaron en styled, de modo que git no puede decidir con que versión ha de quedarse y da conflicto.


5 - El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

En este caso no causó ningún conflicto, porque master no sufrió ningún cambio desde la creación de la rama styled. De este modo git no encontró ningún tipo de problemas a la hora de determinar los cambios entre ambas ramas, y añadió las únicas modificaciones (las de styled).


6 - ¿Qué comando o comandos utilizaste en el paso 25?


>> git log --all --decorate --oneline --graph


7 - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 

Sí porque la rama master no ha sufrido ninguna modificación (no se hizo ningún commit) desde la creación de la rama title. Master tiene su HEAD en el commit padre de la rama title. 


8 - ¿Qué comando o comandos utilizaste en el paso 27?

>> git graph

Para ver el estado del proyecto con sus commits

>> git reset b47630176101cfa7a80dc7e180463a2f0fe17fbc

Sin --hard para no perder los cambios en el working copy


9 - ¿Qué comando o comandos utilizaste en el paso 28? 

En este paso inicialmente me confundí con lo que se pedía y entendí que había que deshacer el deshacer el merge, es decir, rehacer el merge.


Y unas preguntas más abajo me di cuenta que lo que se pedía era eliminar los cambios del woking copy. Habría que hacer:

>> git checkout -- git-nuestro.md


10 - ¿Qué comando o comandos utilizaste en el paso 29? 

>> git branch -d title

Elimino la rama

>> git branch

Compruebo que se ha eliminado


11 - ¿Qué comando o comandos utilizaste en el paso 30? 

Aquí me di cuenta del problema que tuve, que ya comenté en la pregunta anterior. Aquí tendría que hacer:

>> git reflog

Para buscar el commit al que quiero regresar (antes del merge)

>> git reset 9da06a3

Me cambio a ese commit

>> git graph

Compruebo que se ha rehecho el merge


12 - ¿Qué comando o comandos usaste en el paso 32?

>> git reset --hard 7cf21c7c580cc733ba9243bf9de7d7262920b936

Lo hice con --hard para modificar el working copy porque no se especificaba si había que modificarlo o no


13 - ¿Qué comando o comandos usaste en el punto 33?

>> git reflog

Para buscar en el histórico el commit final del merge

>> git reset --hard 9da06a3

Vuelvo al estado final con el título del poema

>> git log

Para comprobar que recuperé todos los datos

>> git graph

Para comprobar que el estado es el mismo que antes de volver al commit inicial.
