# Mi Proyecto

Proyecto individual del curso de DevOps para practicar Git y GitHub.

## Instalacion

1. Clonar el repositorio: git clone https://github.com/Drako426/devops.git
2. Entrar a la carpeta: cd devops

## Comandos usados
- git init: Es para iniciar un repositorio Git vacío en la carpeta del proyecto (crea la carpeta oculta .git/).
- git status: Muestra el estado del repositorio: archivos sin seguimiento, modificados y preparados (staged) para el próximo commit.
- git add: Agrega cambios de un archivo al área de preparación (staging) para incluirlos en el siguiente commit. Ej: git add README.md.
- git commit: Guarda en el historial del repositorio los cambios con un mensaje descriptivo. Ej: git commit -m "Primer commit: agrega README".
- git push: Sube los commits locales al repositorio remoto en GitHub. La primera vez se usó git push -u origin main para enlazar la rama local con la remota.
- git diff: Muestra línea por línea los cambios que se hicieron en los archivos que aún no se han preparado con git add.
- git log: Muestra el historial de commits; con --oneline --graph se ve cada commit en una línea con su hash corto y el gráfico de ramas.
- git restore: Descarta los cambios no preparados de un archivo y lo restaura a su versión del último commit. Ej: git restore notas.txt.
- git restore --staged: Saca un archivo de la preparación sin borrar los cambios, se ve como el archivo vuelve a quedar como "modificado".
- git reset --soft HEAD~1: Deshace el último commit pero conserva sus cambios preparados (staged), se debe usar en commits que aún no se han subido con git push.
- git checkout hash -- archivo: Recupera un archivo tal como estaba en un commit específico del historial. Ej: git checkout d8c90d6 -- README.md.


## Conflicto de merge

El conflicto ocurrió porque rama-python y rama-javascript salieron del mismo commit y ambas modificaron la misma línea de lenguaje.txt con valores distintos. Al fusionar primero rama-python (fast-forward) y luego rama-javascript, Git no pudo decidir automáticamente cual versión conservar. Entonces decidí combinar ambas opciones, dejando "Lenguaje favorito: Python 3.12 y JavaScript", eliminé las marcas de conflicto y confirmé el merge con un commit.
