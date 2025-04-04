# **Actividad 4**
## **Actividad:** Introducción a Git - conceptos básicos y operaciones esenciales## **Actividad:** Introducción a Git - conceptos básicos y operaciones esenciales


### Preguntas

1. ¿Cómo te ha ayudado Git a mantener un historial claro y organizado de tus cambios?  

    Git es muy poderoso, funciona basicamente como una maquina del tiempo en donde puedes ir a momentos especificos donde se ha registrado,es decir, tienes el superpoder de **crear** y **controlar** tu propia linea del tiempo de tu repositorio.

2. ¿Qué beneficios ves en el uso de ramas para desarrollar nuevas características o corregir errores?  

    El uso de ramas es una maravilla, pues te permite crear una linea alterna independiente en donde puedes agregar nuevas funciones o corregir errores en lugar de hacerlo en la linea de tiempo principal y asi evitar arriesgarte si algo sale mal.

3. Realiza una revisión final del historial de commits para asegurarte de que todos los cambios se han registrado correctamente.  
    
        git log --oneline
    
    ![](img/actv4-p3.png)


4. Revisa el uso de ramas y merges para ver cómo Git maneja  múltiples líneas de desarrollo.

        $ git log --graph --oneline
    
    ![](img/actv4-p4.png)

### **Ejercicios**

#### **Ejercicio 4**

1. Hacer cambios en el archivo main.py:
    - Edita el archivo main.py para introducir un nuevo cambio:

        ![](img/actv4-ejc4-1-1.png)

    - Añade y confirma los cambios:

        ![](img/actv4-ejc4-1-2.png)

2. Usar git reset para deshacer el commit:
    - Deshaz el commit utilizando git reset para volver al estado anterior:

        ![](img/actv4-ejc4-2.png)

3. Usar git restore para deshacer cambios no confirmados:
    - Realiza un cambio en README.md y no lo confirmes:
        ![](img/actv4-ejc4-3-1.png)

    - Usa git restore para deshacer este cambio no confirmado:
        ![](img/actv4-ejc4-3-2.png)    

#### **Ejercicio 5**
