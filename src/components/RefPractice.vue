
<script setup>
import {ref} from 'vue'
const a= ref('abc') 
const b = 'xyz'
b='bca'
console.log(  'b value: ' ,b,'a value: ',a.value)
a.value = 'bcd'
console.log( 'again a value: ', a.value)
// export default {
//     data:{

//     },
//     methods: {
//         getData(){
//             //to create focus on input
//             this.$refs.input.focus()
//             //access the value of input
//             let userInput = this.$refs.input.value;
//             console.warn(userInput)
//             //to change the style of input
//             this.$refs.input.style.color= 'green'
//         }
//     }
// }
// window.addEventListener('keydown', function(e){
//    if(e.key === "Enter")
//    {
//     getData();
//    }
// } )
</script>

<template>
    
<input type="text" ref="input"/>
<button v-on:click="getData">Click me</button>
</template>


<style>

</style>


