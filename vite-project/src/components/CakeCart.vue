<template>
  <div class="order">
    <ul class="list">
      <li class="info">{{ order }} ~~~~ ${{ price }}</li>  
    </ul>
  </div>
</template>

<script>
export default {
  name: "Cart",
  props: {
      order: String,
      price: Number,
  },
  methods: {
  }
}
</script>

<style>
.list {
  list-style: none;
  font-size: 1.1rem;
}
.order {
  display:flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
</style>