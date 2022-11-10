<template>
    <div>
        Hola
    </div>
</template>

<script>
// la funcio suma amb es5
function suma(a,b){
    return a + b
}
// us de la funcio 

console.log(suma(10,20))

var sumaEs6 = (a,b) => a + b
console.log("Suma amb es6 es ", sumaEs6(2,3))

var sumaEs6_2 = (a,b) => a + b
console.log(sumaEs6_2(3,5))
let edat = 15
</script>