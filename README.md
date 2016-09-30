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

#VimTutor
                            Lesson 2 SUMMARY


  1. To delete from the cursor up to the next word type:    dw
  2. To delete from the cursor to the end of a line type:    d$
  3. To delete a whole line type:    dd

  4. To repeat a motion prepend it with a number:   2w
  5. The format for a change command is:
               operator   [number]   motion
     where:
       operator - is what to do, such as  d  for delete
       [number] - is an optional count to repeat the motion
       motion   - moves over the text to operate on, such as  w (word),
                  $ (to the end of line), etc.

  6. To move to the start of the line use a zero:  0

  7. To undo previous actions, type:           u  (lowercase u)
     To undo all the changes on a line, type:  U  (capital U)
     To undo the undo's, type:                 CTRL-R

