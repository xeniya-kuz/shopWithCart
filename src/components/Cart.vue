<template>
  <details class="details-my-account">
    <summary class="cart-card">
      <img class="cart" src="css/img/cart.svg" alt="cart" />
      <div class="cart-count">{{ quantity }}</div>
    </summary>

    <div class="my-account-menu">
      <div class="my-account-menu-box">
        <CartItem
          v-for="item of cart"
          :key="item.id"
          v-bind:cart_item="item"
          @remove-from-cart="remove"
        />
      </div>
      <div class="cost">
        <p>TOTAL</p>
        <p>{{ sum }}</p>
      </div>
      <a href="checkout.html" class="my-acc-button">Checkout</a>
      <a href="shopping-cart.html" class="my-acc-button">Go to cart</a>
    </div>
  </details>
</template>

<script>
import CartItem from "@/components/CartItem";

export default {
  name: "Cart",
  props: ["cart"],
  data() {
    return {
    };
  },
  components: {
    CartItem,
  },
  methods: {
    remove(id) {
      this.$emit("remove-from-cart", id);
    },
  },
  computed: {
    sum() {
      let cost = 0;
      this.cart.forEach((el) => {
        cost += el.price * el.count;
      });
      return cost;
    },

    quantity() {
      let counter = 0;
      this.cart.forEach((el) => {
        if (el.count != 1) {
          counter += el.count - 1;
        }
      });
      let total = this.cart.length + counter;
      return total;
    },
  },
};
</script>

