#Conflicto Ejercicio 5
##Descripción del conflicto:
Se produjo un conflicto al intentar hacer merge entre "feature-conflicto" y "main"

###Causa:
Se modificaron la misma línea en ambas ramas.

"main": Texto 2 prueba conflicto
"feature-conflicto": Texto prueba 1 pra conflicto

##Resolución:

1.Detectar el conflicto cuando se realia el git merge
2.Abrir archivo md
3.Identificar marcadores de conflicto
4.Elegir solución adecuada (opcion 1,2 o amabas combinadas)
5.Quitar marcadores de conflicto
6.Guardar el archivo solucionado
	git add ntoas.md
7.Completar merge
	git commit -m merge "************"
8.Subir los cambios
	git push origin main

##Resultado final
Se resolvió el conflicto combinando las dos ramas.

