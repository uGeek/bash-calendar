# Bash Calendar

Este es un script de shell simple que generará un calendario HTML con imágenes y una lista opcional de notas.

Archivos que necesitarías primero:

fotos - nombradas 01.jpg- 12.jpg, una por cada mes
descripciones de la imagen [opcional] - nombrada 01.txt- 12.txt, una por cada mes
listas opcionales de eventos

## Crear lista de eventos
Cada lista de eventos está en un archivo separado con extensión de lista. Contiene personalización de estilo opcional y lista de eventos. Los eventos podrían volver a ocurrir cada año o solo específicos de un año. Aquí hay una lista de ejemplos de eventos:

```
style=color: red;
01-01 New Year
12-25 Christmass
2016-03-28 Easter Monday
2017-04-17 Easter Monday
```

## Uso
Simplemente coloque todas las imágenes en el directorio con el script. Opcionalmente ponga su descripción y sus listas de eventos personalizados. Luego, simplemente puede ejecutar el script y el script generará una página html con el calendario para el próximo año. Puede personalizar el inicio exportando START variables. Algo como esto:

```
START="2016-04-01" ./generate-calendar.sh > cal.html
```

```
./calendar.sh 2019-09-01 > cal.html
```

## Localización
Para generar el calendario, el script usa el datecomando para obtener nombres para los meses y días de la semana. Por lo tanto, antes de ejecutarlo, asegúrese de tener el conjunto de configuración regional correcto (utf-8 one).
