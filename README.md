# Leccion20

**Pregunta 1**

Modificar el siguiente script usando closures para que se ejecute sin problemas.
var num2 = 0;

function suma(num1) {  
	return function() {  
		return num1 + num2;
	}
} 

var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado

var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.

**Solución**
> function suma(num1) {      
      	return function(num2) {  
		return num1 + num2;  
	}  
} 
  var suma2 = suma(2);  
  console.log(suma2(5)); // Debería mostrar 7 de resultado
  var suma12 = suma(12);
  console.log(suma12(76)) // Debería mostrar 88 de resultado.

**Explicación**

En el primer caso toma la variable global var num2=0 , la solución propuesta fue ingresar esa variable como parametro de la función.
