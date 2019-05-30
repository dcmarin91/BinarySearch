# Ejercicios Busqueda y Objetos

## Ejercicio 1 Busqueda Binaria
```
function binarySearch(arr,elem){
	return binaryRecursive(arr,elem,0,arr.length);

 function binaryRecursive(arr,elem,pi,pf){
  	if(pi>pf){
    	return -1
    }
    let mitad = pf-pi/2
    	if(mitad === elem){
    		return mitad
    }
    if(mitad<elem){
      	return binaryRecursive(arr, elem, mitad+1, pf)
    }
    if(mitad>elem){
    	return binaryRecursive(arr, elem, pi, mitad-1)
    }
  }
}
```

## Ejercicio 2 Funcion Constructora Persona

```
function Persona(nombre, peso, altura){
 this.nombre = nombre
 this.peso = peso
 this.altura = altura
}

Persona.prototype.saludar = function(nombre){
	return `Hola ${nombre} me llamo ${this.nombre}`
}

Persona.prototype.bmi = function(){
	return (this.peso)/(this.altura*2)
}
```
## Ejercicio 3 Funcion Constructora Auto

```
function Auto(){
	this.velocidad = 0
}

Auto.prototype.acelerar = function(num){
	this.velocidad += num
}

Auto.prototype.frenar = function(num1){
	this.velocidad -= num1
	if(this.velocidad<0){
  	this.velocidad = 0
  }
  console.log(this.velocidad)
}
```
