# JavaScript 🤡

### JSON

```javascript
my_json = {
	'name': 'john',
	'age': 31,
	'cars': [
		{'name': 'mazda', 'ref': ['3', '6', 'RX-5']},
		{'name': 'chevrolet', 'ref': ['camaro', 'aveo', 'spark']},
		{'name': 'ford', 'ref': ['explorer', 'fusion', 'mustang']}
	]
}
```

#### var, let, const

>El alcance de **var** es global sin importar donde se declare
>El alcance de **let** se limita al bloque donde se declara, **let** reduce el alcance de la variable
>**const ** tiene el mismo alcance de **let** solo que no se deja modificar

```javascript
var alguien = {
    nombre   : 'Pepito',
    apellido : 'Putin',
    edad     :  26
}

function esMayorDeEdad(persona){
    let mensaje
	const MAYORIA_DE_EDAD = 18
    if(persona.edad >= MAYORIA_DE_EDAD) {
        mensaje = 'Es mayor de Edad'
    } else {
        mensaje = 'Es menor de Edad'
        var mensaje2 = 'es cierto'
    }
    console.log(mensaje)
    console.log(mensaje2)
}

esMayorDeEdad(alguien)

```

>Por ejemplo el alcance de **var mensaje2** de la linea 13 abarca todo el codigo, no importa si el flujo de la ejecución no entra en el else donde esta ese var no bota error si se intenta imprimir **mensaje2** ya que js detecta la declaracion de **var mensaje2**

>El alcance de **let mensaje** se limita al cuerpo de la funcion si se intenta usar la variable fuera del cuerpo de la funcion va a botar un error de que la variable no esta declarada

#### Modificar un array const 
```javascript
const numeros = [12, 23, 32, 88, 90, 99]
console.log(numeros)

numeros.push(89)
console.log(numeros)

// el output es [12, 23, 32, 88, 90, 99, 89]
```
> La unica forma de modificar un array de const es haciendo un **push()**

>**CONCLUSIONES**
lo mejor es reducir el alcance de las variables por lo que es mejor practica hacer uso de **let** y **const** que de **var**
