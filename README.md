# Ticket de salida 3

Nombre: Antonia Verdugo Cervela

Rol: 202573048-0

## Errores

### Error 1 
- Tipo de error: Falta inicizar fila del promedio
- Línea del código: linea 36.
- Corrección:

promedio[i]=0;

### Error 2
- Tipo de error: falta hacer free de caja, y a cada posicion (solo q ahora en el main).
- Línea del código: final del codigo, donde estan los demas free. 
- Corrección:

for(int i = 0; i < f; i++){
    free(caja[i]);
}
free(caja);

### Error 3
- Tipo de error: Se accedió fuera del limite, en la función "estaOrdenada".
- Línea del código: línea 19.
- Corrección:

int estaOrdenada(int *plata, int f){
    int ordenada = 1;
    for(int i = 0; i < f-1; i++){
        if(plata[i] < plata[i + 1]){
            ordenada = 0;
        }
    }
    return ordenada;
}


### Error 4
- Tipo de error: Se accede a memoria fuera dell arreglo en acum.
- Línea del código: línea 68
- Corrección:

int *acum = malloc((f+1) * sizeof(int));

## Caso de prueba propio (case_04)

Explicación:

Fila 1: 100 + 50 = 150, 2 monedas, promedio= 75
Fila 2: 10 + 40 = 50, 2 monedas, promedio= 25

Como 150 >= 50, caja esta ordenada


Compra 1 ($200) -> las dos filas alcanzan los 200, por lo tanto alcanza hasta la fila 2. (Compra q cuesta exactamente tada la plata de la caja)

Compra 2 ($201) -> no alcanza, ya q la cja solo contiene 200
