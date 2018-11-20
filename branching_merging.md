# Branching and merging

Los siguientes ejercicios los debes realizar en tu máquina real, no es necesario que los subas a un repositorio en github. Indica los pasos seguidos para realizar cada ejercicio en este mismo fichero.

1. Crea un directorio llamado _**branch_time**_
2. Cámbiate a dicho directorio.
3. Inicializa un repositorio vacío.
4. Crea un fichero llamado first.txt después añade y haz commit con un solo comando.
5. Crea una nueva rama llamada _**amazing_feature**_.
6. Cámbiate a dicha rama.
7. Crea un nuevo fichero llamado best.txt con el contenido "this is the best file".
8. Añade el fichero al área de preparación.
9. Haz commit del fichero con el mensaje "added best.txt".
10. Vuelve a la rama master.
11. Une (merge) la rama feature a la rama master.
12. Borra la rama feature.
13. Crea la rama _**conflict**_ y cámbiate a ella con un solo comando.
14. Crea tu propio conflicto al mezclar dos ramas! Para ello trabaja en el mismo fichero en dos ramas separadas y une (merge) las dos ramas. Arregla los conflictos y finaliza la unión. En el mundo real nunca intentarás crear un conflicto en una unión de ramas, pero es importante que no te sientas intimidado por los conflictos al realizar una unión de ramas y ser capaz de arreglarlos con confianza.

RESPUESTAS

      1. mkdir branch_time
      2. cd branch_time
      3. git init
      4. touch first.txt && git add first.txt && git commit -m "Primer commit"
      5. git branch amazing_feature
      6. git checkout amazing_feature
      7. echo "this is the best file" > best.txt
      8. git add best.txt
      9. git commit -m "added best.txt"
      10. git checkout master
      11. git merge amazing_feature
      12. git branch -d amazing_feature
      13. git checkout -b conflict
      14. Una vez dentro de la rama conflict he editado el fichero first.txt, añadido al área de preparación y hecho commit, despúes me he cambiado a la rama master donde también he editado el fichero y añadido otro contenido, guardado en el área de preparación y hecho commit, al intentar hacerle el git merge con la rama conflict me da error.
      Para corregir el problema al abrir el fichero que me daba error aparecían las diferencias, al editarlo para que sean iguales y hacerle commit nuevamente ya no da error.
