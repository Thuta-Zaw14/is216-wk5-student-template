<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const newItem = ref()

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item,index) in items" :key="index">{{item}} 
            <button v-on:click="items.splice(index,1)">Delete</button>
        </li>
     </ul>


    <input v-on:keyup.enter="items.push(newItem);newItem=''" type = "text" v-model="newItem">
    <button v-on:click="items.push(newItem);newItem=''">Add!</button>

   
</template>
