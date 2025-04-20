# **Actividad:Rebase, Cherry-Pick y CI/CD en un entorno ágil**

## **Parte 1: git rebase para mantener un historial lineal**

1. **Introducción a Rebase:**

   El rebase mueve tus commits a una nueva base, dándote un historial lineal y limpio. En lugar de fusionar ramas y mostrar un "commit de merge", el rebase integra los cambios aplicándolos en la parte superior de otra rama.

   - **Caso de uso**: Simplifica la depuración y facilita la comprensión del historial de commits.

2. **Escenario de ejemplo:**

   1. **Crea un nuevo repositorio Git y dos ramas, main y new-feature:**

      ![](img/act6-1-2-1.png)
     
      ![](img/act6-1-2-2.png)

      **Codigo**

        ```bash
        $ mkdir try-git-rebase
        $ cd try-git-rebase
        $ git init
        $ echo "# Mi Proyecto de Rebase" > README.md
        $ git add README.md
        $ git commit -m "Commit inicial en main"
        ```

   2. **Crea y cambia a la rama new-feature:**

        ![](img/act6-1-2-3.png)

        **Codigo**

        ```bash
        $ git checkout -b new-feature
        $ echo "Esta es una nueva característica." > NewFeature.md
        $ git add NewFeature.md
        $ git commit -m "Agregar nueva característica"
        ```
    **Pregunta:** Presenta el historial de ramas obtenida hasta el momento.

    *Historial Limpio*
     ![](img/act6-1-2-4.png)

   **Ahora, digamos que se han agregado nuevos commits a main mientras trabajabas en new-feature:**

    ![](img/act6-1-2-5.png)

    *Codigo:*
    
   ```bash
   # Cambiar de nuevo a 'main' y agregar nuevos commits
   $ git checkout main
   $ echo "Updates to the project." >> Updates.md
   $ git add Updates.md
   $ git commit -m "Update main"
   ```

   **Tu gráfico de commits ahora diverge (comprueba esto)**

    *Efectivamente, existe una divergencia entre las ramas*
    ![](img/act6-1-2-6.png)

   > **Tarea**: Realiza el rebase de `new-feature` sobre `main` con los siguientes comandos:

    ![](img/act6-1-2-7.png)

    *Codigo*

    ```bash
    $ git checkout new-feature
    $ git rebase main
    ```

3. **Revisión:**

   Después de realizar el rebase, visualiza el historial de commits con:
   ```bash
   $ git log --graph –oneline
   ```
    *Visualizacion del historial, se observa un adelantamiento de la rama new-feauture sobre la rama main*. **Podemos decir que esta listo para una fusion limpia**
   ![](img/act6-1-3.png)

4. **Momento de fusionar y completar el proceso de git rebase:**
   ```bash
   # Cambiar a 'main' y realizar una fusión fast-forward
   $ git checkout main
   $ git merge new-feature
   ```
   *Fusion limpia realizada*
    ![](img/act6-1-4-1.png)

   Cuando se realiza una fusión *fast-forward*, las HEADs de las ramas main y new-feature serán los commits correspondientes.

    **Ambas estan apuntando al mismo commit "niveladas"**
    ![](img/act6-1-4-2.png)