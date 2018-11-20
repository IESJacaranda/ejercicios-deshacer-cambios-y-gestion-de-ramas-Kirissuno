# Ejercicios Checkout y Reset

Los siguientes ejercicios los debes realizar en tu máquina real, no es necesario que los subas a un repositorio en github. Indica los pasos seguidos para realizar cada ejercicio en este mismo fichero.

1. Crea un directorio llamado _**destruction**_
2. Cámbiate a dicho directorio
3. Inicializa un repositorio git vacío.
4. Crea un fichero llamado **stage_me.txt**
5. Añade el fichero stage_me.txt al área de preparación (staging area).
6. Mueve el fichero stage.txt del área de preparación al directorio de trabajo.
7. Añade el fichero stage_me.txt al área de preparación.
8. Elimina el fichero stage_me.txt del área de preparación y del directorio de trabajo.
9. Crea un fichero nuevo llamado commit_me.txt.
10. Añade el fichero commit_me.txt al área de preparación.
11. Haz un commit con el mensaje "adding commit_me.txt"
12. Crea otro fichero llamado second.txt.
13. Añade el fichero second.txt al área de preparación.
14. Haz commit con el mensaje "adding second.txt".
15. Muestra los commits previos uno por línea mostrando el identificador únicao (SHA) y el comentario asociado.

Para realizar los siguientes ejercicios debes investigar sobre los parámetros --soft --mixed y --hard del comando git reset.

16. Utilizando git reset, deshaz el commit previo y devuelve los cambios al directorio de trabajo.
17. Añade el fichero second.txt otra vez al área de preparación.
18. Haz un commit con el mensaje "Trying to commit again".
19. Utilizando git reset deshaz el commit previo y devuelve los cambios al área de preparación.
20. Haz commit con el mensaje "Trying to commit again and again".
21. Utilizando git reset deshaz el commit previo para que ningún cambio aparezca en el directorio de trabajo.
22. ¡Date una palmadita en la espalda! ¡Acabas de realizar un flujo de trabajo bastante complejo de git!
    
    RESPUESTAS
    
        1. mkdir destruction
        2. cd destruction
        3. git init
        4. touch stage_me.txt
        5. git add stage_me.txt
        6. git rm --cached stage_me.txt
        7. git add stage_me.txt
        8. git rm -f stage_me.txt  // **He tenido que forzar porque no dejaba quitarlo sin --cache o -f.**
        9. touch commit_me.txt
        10. git add commit_me.txt
        11. git commit -m "adding commit_me.txt"
        12. touch second.txt
        13. git add second.txt
        14. git commit -m "adding second.txt"
        15. git log --oneline
        16. git reset --mixed COD_COMMIT
        17. git add second.txt
        18. git commit -m "Trying to commit again"
        19. git reset --soft COD_COMMIT
        20. git commit -m "Trying to commit again and again"
        21. git reset --hard COD_COMMIT
