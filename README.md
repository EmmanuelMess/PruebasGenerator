[![Build Status](https://travis-ci.org/EmmanuelMess/PruebasGenerator.svg?branch=master)](https://travis-ci.org/EmmanuelMess/PruebasGenerator) [![Coverage Status](https://coveralls.io/repos/github/EmmanuelMess/PruebasGenerator/badge.svg?branch=master)](https://coveralls.io/github/EmmanuelMess/PruebasGenerator?branch=master) [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/EmmanuelMess/PruebasGenerator/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/EmmanuelMess/PruebasGenerator/?branch=master)

# PruebaGenerator

Este es un generador de temas a partir de un archivo YAML, con el sigiente formato:

```YAML
preguntas:
  - descripcion: El término pixel hace referencia a
    respuestas_correctas:
      - La unidad mínima de información de una imagen.
    respuestas_incorrectas:
      - La longitud de la diagonal de una imagen en pulgadas.
    ocultar_opcion_todas_las_anteriores: true
    ocultas_opcion_ninguna_de_las_anteriores: true
    
  - descripcion: El término pixel hace referencia a
    respuestas_correctas:
      []
    respuestas_incorrectas:
      - La longitud de la diagonal de una imagen en pulgadas.
    texto_ninguna_de_las_anteriores: "Ninguna!"
``` 

Genera una cantidad de temas, de los cuales se puede descargar la version a resolver y la resuelta.

Para usarlo:

```bash
git clone https://github.com/EmmanuelMess/PruebasGenerator.git
cd "PruebasGenerator/src"
php -S localhost:8080
```

Y abre`http://localhost:8080/index.php` en un navegador. Despues tendras que arreglar los problemas de ubicacion de archivos que surgen.

## Problemas Conocidos

* No hay forma de limitar la cantidad de preguntas por prueba. Se podria agregar muy facilmente, pero estoy cansado.
* Se rompen las rutas a los archivos muy facilmente, lo que functina a uno no le funciona a otro. Tiene que ver con el hecho de que la ubicacion raiz del servidor tiende a cambiar, de acuerdo a que variable PHP se use.