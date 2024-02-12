<template>
  <div>
    <DeskCard 
      v-for="destination in destinations" 
      :key="destination.name" 
      :Destination="destination"
    />
  </div>
</template>

<script setup>
import DeskCard from "@/components/DeskCard.vue";
const destinations = [
{
        name: "Happy Fairy Pink Unicorn",
        flavor: "Strawberry",
        price: "$88.00",
        image: "/pinkcake.jpg",
    },
    {
        name: "Death Wednesday Goth Black",
        flavor: "Blackberry",
        price: "$88.00",
        image: "/blackcake.jpg",
    },
    {
        name: "Cream Milkshake White Ice",
        flavor: "Pineberry",
        price: "$88.00",
        image: "/whitecake.jpg",
    },
    {
        name: "Fresh Mint Air Water",
        flavor: "Gooseberry",
        price: "$88.00",
        image: "/mintcake.jpg",
    },
    {
        name: "Happy Birthday Pink Fairy",
        flavor: "Raspberry",
        price: "$60.00",
        image: "./public/pinkbday.jpg",
    },
    {
        name: "Happy Brithday Ocean Blue",
        flavor: "Blueberry",
        price: "$60.00",
        image: "./public/bluebday.jpg",
    }
  ]
</script>

<style scoped> </style>
