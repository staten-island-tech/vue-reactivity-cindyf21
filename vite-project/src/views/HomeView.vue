<template>
  <div>
    <CakeCard 
      v-for="destination in destinations" 
      :key="destination.name" 
      :Destination="destination"
    />
  </div>
</template>

<script setup>
import CakeCard from "@/components/CakeCard.vue";
const destinations = [
{
        name: "happy fairy pink unicorn",
        flavor: "strawberry",
        price: "$88.00",
        img: "/pinkcake.jpg",
    },
    {
        name: "death wednesday goth black",
        flavor: "blackberry",
        price: "$88.00",
        img: "/blackcake.jpg",
    },
    {
        name: "cream milkshake white ice",
        flavor: "pineberry",
        price: "$88.00",
        img: "/whitecake.jpg",
    },
    {
        name: "fresh mint air water",
        flavor: "gooseberry",
        price: "$88.00",
        img: "/mintcake.jpg",
    },
    {
        name: "happy birthday pink fairy",
        flavor: "cranberry",
        price: "$60.00",
        img: "/pinkbday.jpg",
    },
    {
        name: "happy birthday ocean blue",
        flavor: "blue raspberry",
        price: "$60.00",
        img: "/bluebday.jpg",
    },
    {
        name: "happy birthday flower pond",
        flavor: "lemon water",
        price: "$75.00",
        img: "/flowerbday.jpg",
    },
    {
        name: "happy birthday sprinkle mint",
        flavor: "mint toothpaste",
        price: "$65.00",
        img: "/sprinklebday.jpg",
    },
    {
        name: "pink blank vertical lines",
        flavor: "pink lemonade",
        price: "$55.00",
        img: "/pinklinecake.jpg",
    },
    {
        name: "painterly pink blue canvas",
        flavor: "rainbow sherbet",
        price: "$90.00",
        img: "/paintcake.jpg",
    },
    {
        name: "double white horizontal lines",
        flavor: "butter pecan",
        price: "$185.00",
        img: "/doublewhitecake.jpg",
    },
    {
        name: "hugs and kisses xoxo",
        flavor: "black cherry",
        price: "$80.00",
        img: "/xoxocake.jpg",
    }
  ]
</script>

<style scoped> </style>
