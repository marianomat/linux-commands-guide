#### Commands structure basics

        command -options arguments

#### Command Arguments

A la vez, tambien aceptan argumentos (cosas que el comando usa)
Ejemplo "ncal may 2004", ncal es un comando que hacepta 2 argumentos, el mes y año y devuelve el calendario". Tambien hay argumentos que aceptan archivos (txt, etc.). Por ejemplo rm ejemplo.txt.

#### Commands Options Syntax

La mayoria de comandos soportan multiples opciones que modifican sus comportamientos. Podemos elegir que opciones usar o no usar ninguna, al momento de ejecurtar un comando.

Estas opciones estan precedidas por un guion "-".

Si hago "ncal -h", cambio el comportamiento de mostrar de otro color que dia es hoy.
o "ncal -j", cuenta los dias desde 1 de enero, por ejemplo el 15 de mayo es el dia 133 del año.

Se admite poner varias opciones a la vez.

    >ncal 3 -h -j
    >2021
    April                   May                     June
    Su      94 101 108 115         122 129 136 143 150     157 164 171 178
    Mo      95 102 109 116         123 130 137 144 151     158 165 172 179
    Tu      96 103 110 117         124 131 138 145     152 159 166 173 180
    We      97 104 111 118         125 132 139 146     153 160 167 174 181
    Th  91  98 105 112 119         126 133 140 147     154 161 168 175
    Fr  92  99 106 113 120         127 134 141 148     155 162 169 176
    Sa  93 100 107 114         121 128 135 142 149     156 163 170 177

Pero una alternativa es combinar las opciones en uno

    >ncal -3hj
    >2021
    April                   May                     June
    Su      94 101 108 115         122 129 136 143 150     157 164 171 178
    Mo      95 102 109 116         123 130 137 144 151     158 165 172 179
    Tu      96 103 110 117         124 131 138 145     152 159 166 173 180
    We      97 104 111 118         125 132 139 146     153 160 167 174 181
    Th  91  98 105 112 119         126 133 140 147     154 161 168 175
    Fr  92  99 106 113 120         127 134 141 148     155 162 169 176
    Sa  93 100 107 114         121 128 135 142 149     156 163 170 177

# Long form opcions

En algunos casos podes elegir que si usar la opcion corta o larga.
En el caso de usar la forma larga, debemos poner 2 guiones "--".

    >date -u es lo mismo que >date --universal

Otra cosa es que si tenes 2 argumentos y usas la forma larga, tenes que ponerlo separados no podes hacer como en la forma corta de agruparlos en un "-".

    >sort colors.txt --reverse --unique NO es lo mismo que >sort colors.txt --reverseunique

# Options con parametros

Algunas opciones requieren que le pasemos parametros como valores adicionales.

Por ejemplo: ncal tiene una opcion -A que se usa para mostrar un cierto numero de meses despues de una fecha especifica (hoy si no especifica). El parametro especifica cuantos meses

    >ncal -A 2

Es valido tambien

    >ncal -A2
