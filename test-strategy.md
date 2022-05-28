Se realizaron los testeos pertinentes y se hicieron pruebas en la interfaz y codigo fuente, se utilizo .net y framwork selenium para testear y verificar el bug en la aplicacion.
Estos fueronn los resultados
1. Al comenzar el codigo fuente en la seccion de  function checkGuess() la condicionate if tenia tres iguales junto con las condicionantes else se procedio a corregirlo 
para hacer la igualdad a 1, quedando de esta forma.
 Error: if(userGuess === randomNumber) {
        else if(guessCount === ATTEMPS) {
 Correccion: if(userGuess == randomNumber) {
             else if(guessCount == ATTEMPS) {

2. En la primera condicionante en la linea de codigo siguiente:
if(userGuess == randomNumber) {
      lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'black';
      lowOrHi.textContent = '';
      setGameOver();

Se tenia erroneo el resultado del background y se cambio a Rojo como especifica las instrucciones quedando de la siguiente manera:
if(userGuess == randomNumber) {
      lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'Rojo';
      lowOrHi.textContent = '';
      setGameOver();

3. En la seguda condicion la linea de codigo de background esta de color rojo
 } else if(guessCount == ATTEMPS) {
      lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
      
 Se procedio a hacer el cambio del background a color verde
  } else if(guessCount == ATTEMPS) {
      lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'verde';
      setGameOver();

4. En la ultima condicionante el background estaba de color verde y las condicionates estaban al reves de esta forma:
} else {
      lastResult.textContent = 'Incorrecto! ';
      lastResult.style.backgroundColor = 'green';
      if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      }
    }
 Se procedio a cambiar  el background a color negro como estaba en el requerimiento y el primer if the sea condicionante se cambio a Mayor que, y la segund a 
 menor que, quedando de la siguiente manera.
 } else {
      lastResult.textContent = 'Incorrecto! ';
      lastResult.style.backgroundColor = 'green';
      if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      }
    }
    
El codigo fuente lo encontraran con el nombre index.html al correrlo podran verificar que la interfaz funciona correctamente.

