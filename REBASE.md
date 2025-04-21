# **Tarea 1: Validación automática con GitHub Actions**
## **Uso de REBASE**
1. Primero editamos el historial con `git rebase -i` para luego reemplazar "pick" por "reword" de los commit a modificar mensaje.
2. Guardamos, y al salir nos irá pidiendo cada nuevo mensaje, guardamos y salimos repetidas veces tanta sea la cantidad de commits.
3. Asi ya tenemos nuevos mensajes a los últimos 3 commits que en nuestro caso va asociado al seguimiento de 3 archivos txt (archivotxt_1_X) y lo validamos con `git log -p`
4. Procedemos luego a realizar una fusión de estos 3 commits. Volvemos a editar el historial con `git rebase -i` pero en este caso editaremos los últimos 2 commits reemplazando "pick" por "squash", comando para fusionar commit locales.
5. Tener en cuenta que el primero de esos 3 commits permanece igual pues será el que quedará para la fusión con los otros 2.
6. Guardamos y cerrar donde luego nos pedirá el nuevo mensaje del commit que abracará la fusión.
7. Aplicamos `git push -- force`, más aún si ya se había realizado un "push" con los commit que modificamos.