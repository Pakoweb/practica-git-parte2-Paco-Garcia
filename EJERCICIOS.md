# Resumen de Comandos Git - Ejercicios

## Ejercicio 1: Ciclo básico de Git

```bash
# Crear archivo notas.md con asignaturas
echo "- Asignatura 1" > notas.md

# Añadir archivo al staging
git add notas.md

# Crear commit con mensaje
git commit -m "feat: añade notas iniciales"

# Subir cambios a GitHub
git push origin main

# Editar notas.md y añadir más asignaturas
# Hacer commit directo de todos los cambios en tracked files
git commit -am "feat: amplía notas.md"
git push origin main

## Ejercicio 2: Ramas

# Crear nueva rama y cambiar a ella
git checkout -b feature-tareas

# Editar notas.md y añadir tareas pendientes
git add notas.md
git commit -m "feat: añade lista de tareas pendientes"

# Subir rama al remoto y establecer upstream
git push -u origin feature-tareas

# Volver a main y fusionar cambios
git checkout main
git merge feature-tareas
git push origin main

# Borrar rama local y remota
git branch -d feature-tareas
git push origin --delete feature-tareas

##Ejercicio 3: Borrado y restauración
# Crear archivo temporal y añadirlo al repo
echo "contenido temporal" > temporal.txt
git add temporal.txt
git commit -m "chore: añade archivo temporal"
git push origin main

# Borrar archivo y hacer commit
git rm temporal.txt
git commit -m "chore: elimina archivo temporal"
git push origin main

# Restaurar archivo desde último commit
git restore temporal.txt

##Ejercicio 4: Logs y diffs
# Hacer 2 commits modificando notas.md
git add notas.md
git commit -m "feat: cambio 1 en notas.md"
git commit -am "feat: cambio 2 en notas.md"

# Ver historial resumido y gráfico de commits
git log --oneline --graph --all

# Ver diferencias entre último commit y el anterior
git diff HEAD~1 HEAD

##Ejercicio 5: Conflictos intencionados
# Crear rama para generar conflicto
git checkout -b feature-conflicto

# Editar notas.md en main y en feature-conflicto en la misma línea
# Intentar fusionar ramas y resolver conflicto manualmente
git checkout main
git merge feature-conflicto

# Marcar archivo resuelto y hacer commit
git add notas.md
git commit -m "feat: resuelve conflicto en notas.md"

# Documentar resolución de conflicto
echo "Se resolvió el conflicto eligiendo la versión correcta de la línea conflictiva" > conflicto.md
git add conflicto.md
git commit -m "docs: documenta resolución de conflicto"
git push origin main

##Ejercicio 6: Tags
# Crear tag ligero y subirlo al remoto
git tag v1.0
git push origin --tags

# Crear tag anotado con mensaje y subirlo
git tag -a v1.1 -m "Primera versión estable"
git push origin --tags
