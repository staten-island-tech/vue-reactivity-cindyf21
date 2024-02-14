<template>
    <div>
        <h2>{{ Destination.name }}</h2>
        <img :src="Destination.img" alt="">
        <h3>{{ Destination.flavor }}</h3>
        <h3>{{ Destination.price }}</h3>
        <h3>{{ clicked }}</h3>
        <button @click="increment">Add To Cart</button>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps({
    /* define data expected to receive
    age: Number or name: String, */
    Destination: Object,
});

const clicked = ref(0);
function increment(){
    clicked.value++;
}
</script>

<style scoped>
img {
    width: 250px;
    height: 300px; 
    object-fit: cover;
    display: flex;
    justify-content: center ;
}
</style>