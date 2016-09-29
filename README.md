# Codigo Bash para linux

Codigo para buscar 

zcat loc-gowalla_totalCheckins.txt.gz
zgrep -e '-[1-3]0T[0-9]\{2\}:[0-9]\{2\}:19' loc-gowalla_totalCheckins.txt.gz | wc -l

#¿Cómo tratar un string?
Mediante CUT__
1) Concaternar la funcion -> |
2) Separarlo en campos
    El string [] lo divides en "n" campos
    | cut -d$''
3) Proyectar el campo deseado
    Si es Primer campo, | cut -d$'' f1
    Si es Primer y Quinto campo, | cut -d$'' f1,5

Hay las siguientes funciones
| cut -d$'' # --delimitador, lo que separará
-d$'\t' #el separador de campos (limitador) será el TAB (espaciado)
-d$'\r' #el separador de campos (limitador) será el ENTER
-d$'\n' #el separador de campos (limitador) será ¿¿¿???

#¿Cómo tratar un string?
Mediante AWK
1) Concaternar la funcion -> |
2) Separarlo en campos
    El string [] lo divides en "n" campos
    | awk -F'\t'
3) Proyectar el campo deseado
    | awk -F'\t' '{print$4}'
    | awk -F'\t' '{print $1, $2, $3}'


#¿Cómo tratar un string?
El momento que ejecute el comando, 
| awk -F'\t' '{print $1"," $2"," $3}'
