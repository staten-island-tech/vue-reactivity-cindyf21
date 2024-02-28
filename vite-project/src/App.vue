<template>
  <div id="gallery">
    <section id="input">
      <h1> BAKE & CREATE </h1>
      <h2 class="subtitle"> Order Online, Pick Up In Store! </h2>
      <div class="cakeChoices">
        <Card
          class="choice"
          v-for="(cakeChoice, index) in cakeChoices"
          @addCakeList="addCakeList(index)"
          :key="index"
          :cake="cakeChoice.cake"
          :cakeImage="cakeChoice.cakeImage"
          :description="cakeChoice.description"
          :price="cakeChoice.price"
        />
      </div>
    </section>

    <section id="orderList">
      <h2 class="cartLabel"> Shopping Cart: </h2>
      <Cart
        class="cart"
        v-for="(cakeChoice, index) in order"
        :key="index"
        :order="cakeChoice.cake"
        :price="cakeChoice.price"
      />
      <h2 class="cartLabel"> Subtotal: ${{ subtotal }}</h2>
      <button class="deleteBtn" @click="removeLast()"> Delete Last </button> 
      <button class="deleteBtn" @click="removeAll()"> Delete All </button>
    </section>
  </div>
</template>

<script>
import Card from "./components/CakeCard.vue";
import Cart from "./components/CakeCart.vue";
export default {
  cake: "App",
  components: {
    Card,
    Cart,
  },
  data() {
    return {
      subtotal: 0,
      selectedCake: 0,
      cakeChoices: [
      {
        cake: "happy fairy pink unicorn",
        description: "strawberry",
        price: 88,
        cakeImage: "/pinkcake.jpg",
    },
    {
        cake: "death wednesday goth black",
        description: "blackberry",
        price: 88,
        cakeImage: "/blackcake.jpg",
    },
    {
        cake: "cream milkshake white ice",
        description: "pineberry",
        price: 88,
        cakeImage: "/whitecake.jpg",
    },
    {
        cake: "freshly minty airy water",
        description: "gooseberry",
        price: 88,
        cakeImage: "/mintcake.jpg",
    },
    {
        cake: "happy birthday pink fairy",
        description: "cranberry",
        price: 66,
        cakeImage: "/pinkbday.jpg",
    },
    {
        cake: "happy birthday ocean blue",
        description: "blue raspberry",
        price: 66,
        cakeImage: "/bluebday.jpg",
    },
    {
        cake: "happy birthday flower pond",
        description: "lemon water",
        price: 70,
        cakeImage: "/flowerbday.jpg",
    },
    {
        cake: "happy birthday sprinkle mint",
        description: "mint toothpaste",
        price: 66,
        cakeImage: "/sprinklebday.jpg",
    },
    {
        cake: "pink blank vertical lines",
        description: "pink lemonade",
        price: 168,
        cakeImage: "/pinklinecake.jpg",
    },
    {
        cake: "painterly pink blue canvas",
        description: "rainbow sherbet",
        price: 282,
        cakeImage: "/paintcake.jpg",
    },
    {
        cake: "double white horizontal lines",
        description: "butter pecan",
        price: 1314,
        cakeImage: "/doublewhitecake.jpg",
    },
    {
        cake: "hugs and kisses xoxo",
        description: "black cherry",
        price: 520,
        cakeImage: "/xoxocake.jpg",
    },   
      ],
      order: [],
      orderPrice: [],
    };
  },
  methods: {
    addCakeList(index) {
      this.order.push(this.cakeChoices[index]);
      this.orderPrice.push(this.cakeChoices[index].price);
      this.subtotal = this.subtotal + this.cakeChoices[index].price;
    },
    removeLast() {
      if (this.order.length !== 0) {
        this.subtotal = this.subtotal - this.orderPrice[this.orderPrice.length - 1];
        this.order.pop();
        this.orderPrice.pop();
      }
    },
    removeAll() {
      this.order = [];
      this.orderPrice = [];
      this.subtotal = 0;
    },
  },
};
</script>

<style lang="css">
#gallery {
  text-align: center;
  display: flex;
  flex-direction: row;
  background-color: rgb(224, 223, 223);
}
#input {
  width: 68vw;
}
.cakeChoices {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}
section {
  display: flex;
  align-items: center;
  flex-direction: column;
}
#orderList {
  margin: 1rem;
  height: auto;
  background-color: #e9bcbc;
  width: 25vw;
}
h1 {
  margin-top: 3rem;
  margin-bottom: 1rem;
  font-size: 2.8rem;
}
.subtitle {
  font-style: italic;
}
h2 {
  margin-top: 2rem;
}
.cartLabel {
  text-decoration: underline;
}
.deleteBtn {
  margin-bottom: 1rem;
  background-color: black;
  color: white;
}
</style>