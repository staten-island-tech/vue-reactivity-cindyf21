<template>
  <div class="choice">
    <h2 class="name"> {{ cake }} </h2>
    <h2 class="price"> ${{ price }} </h2>
    <img class="image" :src="cakeImage" :alt="description" />
    <h2 class="description"> {{ description }} </h2>
    <button class="addCart" @click="$emit('addCakeList')"> Add to Cart </button>
  </div>
</template>

<script >
export default {
  name: "Card",
  props: {
    cake: String,
    price: Number,
    cakeImage: String,
    description: String,
  },
};
</script>

<style>
.name {
  align-content: center;
  padding-left: 1rem;
  padding-right: 1rem;
  margin-top: 2rem;
  font-size: 20px;
}
.price {
  margin-top: 0.2rem;
  margin-bottom: 0.2rem;  
  font-size: 18px;
}
.image {
  height: 18rem;
  width: 20rem;
  object-fit: cover;
  display: block;
  margin-left: 1rem;
  padding: 1rem;
}
.description {
  align-content: center;
  margin-top: 0.2rem;
  color: #da5a5a;
  font-size: 18px;
  font-style: italic;
}
.choice {
  display: flex;
  flex-direction: column;
  width: 20vw;
  background-color: white;
  margin-left: 1.5rem;
  margin-right: 0.2rem;
  margin-top: 3rem;
}
.addCart {
  background-color: rgb(0, 0, 0);
  color: white;
}
</style>



