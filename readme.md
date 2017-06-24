1. git init

2. nano git-nuestro.md

3. git add git-nuestro.md

4. git commit -m "Creo archivo git-nuestro.md"

5. git branch styled

6. git branch

7. git checkout styled

8. git status

9. nano git-nuestro.md

10. git add git-nuestro.md - git commit -m "Modifico archivo git-nuestro.md desde rama styled"

11. - ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
Deshace el último commit gracias al parámetro HEAD virgulilla uno y lo que había en mi Working Copy gracias al parámtro hard, el Staging Area queda vacío.

12. - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reflog -> Para localizar el id del commit que había deshecho
git reset --hard ID_COMMIT -> Rehago el commit y modifico el working copy con parametro hard. Al usar reset muevo los punteros HEAD y MASTER al commit recuperado

13. git merge master
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No, pues la rama en la que estoy, styled, contiene ya todos los cambios de la rama master; master es padre de stylus.

14. git checkout master
15. git branch htmlify
16. git checkout htmlify
17. nano git-nuestro.md
18. git add git-nuestro.md - git commit -m "Modifico archivo gi-nuestro.md en rama htmlify"

19. git checkout styled - git merge htmlify

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si, porque git detecta que el mismo archivo mergeado tiene lineas distintas y no sabe como debe unirlas. Por tanto, para resolverlo editamos el archivo, nos quedamos con el contenido de la rama styled y luego añadimos al staging area y hacer luego un commit.

20. nano git-nuestro.md
git add git-nuestro.md
git commit

21. git checkout master
git merge styled
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No se produce conflicto debido a que nuestra rama master realiza un merge de tipo fast forward, commit alineados como una lista, y se posiciona arriba del todo junto a la rama styled y cogiendo sus cambios sin necesidad de realizar un nuevo commit.

22. git checkout -b title
23. nano git-nuestro.md -  git add git-nuestro.md - git commit -m "Modifico el archivo git-nuestro.md incluyendo un titulo en rama TITLE"
24. git checkout master

25. - ¿Qué comando o comandos utilizaste en el paso 25?
Me he creado un alias para dibujar el diagrama y asi poder usarlo rapidamente cuando lo necesite usando el siguiente comando:
git config alias.graph "log --graph --decorate --pretty=oneline"

26. git merge --no-ff title
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí, porque la rama TITLE tiene los cambios contenidos en la rama MASTER y ambos se encuentran alineados en lista

27. - ¿Qué comando o comandos utilizaste en el paso 27?
git reset HEAD~1

28. - ¿Qué comando o comandos utilizaste en el paso 28?
git checkout -- git-nuestro.md

29. - ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title

30. - ¿Qué comando o comandos utilizaste en el paso 30?
git reflog //Localizo el id del commit donde mergeé con la rama title que tenia los cambios
git reset --hard ID_COMMIT

31. git checkout - git branch -D htmlify - git branch -D styled

32. - ¿Qué comando o comandos usaste en el paso 32?
git reflog // Para localizar el id del primer commit y luego hacer un reset para mover HEAD y MASTER al inicio
git reset --hard ID_COMMIT

33. - ¿Qué comando o comandos usaste en el punto 33?
git reflog // Para localizar el id del commit y luego hacer un reset para mover HEAD y MASTER al commit deseado
git reset --hard ID_COMMIT

34. git reflog - git checkout ID_COMMIT - git tag inicial(styled, htmlify, title)

35. git checkout htmlify
