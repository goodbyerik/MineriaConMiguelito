# Codigo Bash para linux

Codigo para buscar 

zcat loc-gowalla_totalCheckins.txt.gz
zgrep -e '-[1-3]0T[0-9]\{2\}:[0-9]\{2\}:19' loc-gowalla_totalCheckins.txt.gz | wc -l

#¿Cómo tratar un string?
Mediante CUT <br />
<li>
1) Concaternar la funcion -> | <br />
2) Separarlo en campos <br />
<ul>El string [] lo divides en "n" campos </ul>
    | cut -d$''
3) Proyectar el campo deseado<br />
    Si es Primer campo, 
    | cut -d$'' f1 
    Si es Primer y Quinto campo, 
    | cut -d$'' f1,5 <br />
</li>
Hay las siguientes funciones<br />
| cut -d$'' # --delimitador, lo que separará<br />
-d$'\t' #el separador de campos (limitador) será el TAB (espaciado)<br />
-d$'\r' #el separador de campos (limitador) será el ENTER<br />
-d$'\n' #el separador de campos (limitador) será ¿¿¿???<br />

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
