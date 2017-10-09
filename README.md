<h1> **My New App isValidCard**
<h4> Este es el README de mi nueva aplicación isValidCard

> Creamos una función llamada _isValidCard_ la cual va a ser invocada para validar el númeo de la tarjeta de credito ingresada por el usuario mediante un _prompt_.
>> Para lo cual utilizamos el _Algorítmo de Luhn_ o también conocido como _Algorítmo de módulo 10_.

>El _Algortimo luhn_ es una fórmula de suma de verificacion que es utilizada para validar una diversidad de números de identificación.

>Una vez que obtengo el número de la tarjeta ingresada por el usuario, agregamos el número de la tarjeta en un _array_ pero en orden invertido. Luego a todos lo números en posiciones par se les debe multipicar por _2_, si el resultado de la multiplicación es mayor igual a _10_ entonces debemos sumar sus dígitos.
>>Luego sumamos los números de las nuevas posiciones pares e impares se mantienen, una vez que obtengo el resutado de la suma total debemos obtener el residuo de la división entre _10_.

> Si el residuo de la division entre _10_ es _cero_ entonces decimos que el numero de la tarjeta de crédito es válida.

PSEUDOÓDIGO |  
> funcion isValidCard(sixteenDigitString){
>  reverse = 0;
>  resto = 0;
>  do{
>   reverse = reverse * 10 + (resto % 10);
>  } mientras ( resto > 0 )
    var numSum = 0;
    var value;
    para (var i = 1; i <= 16; i++) {
       si  (i % 2 === 0) {
           value = 2 * reverse[i];
           si (value >= 10) {
               value = (Math.floor(value / 10) + value % 10);
           }
       } caso contrario {
           value = +reverse[i];
       }
       numSum += value;
   }
   return  (numSum % 10 === 0 ? 'Tarjeta de Crédito Válida' : 'Tarjeta de Crédito no Válida');
}
isValidCard;
isValidCard
