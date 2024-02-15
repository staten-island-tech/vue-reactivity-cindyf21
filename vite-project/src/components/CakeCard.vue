<template>
    <div>
        <h2>{{ Destination.name }}</h2>
        <img :src="Destination.img" alt="">
        <h3>{{ Destination.flavor }}</h3>
        <h3>{{ Destination.price }}</h3>
        <h3>{{ clicked }}</h3>
        <button @click="increment">Add to Cart</button>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps({
    // define data expected to receive - age: Number, name: String,
    Destination: Object,
});

const clicked = ref(0);
function increment(){
    clicked.value++;
}
</script>

<style scoped>
img {
    width: 300px;
    height: 320px; 
    object-fit: cover;
    display: flex;
    justify-content: center ;
    margin-left: auto;
    margin-right: auto;
    padding: 1rem;
}
h2 {
    font-weight: bold;
    text-align: center;
}
h3 {
    text-align: center;
}
button {
    margin-left: 25rem;
}
</style>