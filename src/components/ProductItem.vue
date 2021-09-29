<template>
  <div class="item">
    <a class="product-card"
      href="single-page.html">
      <img
        class="product-img"
        :src="product_item.imageUrl"
        :alt="product_item.name"
      />
      <p class="product-text">{{ product_item.name }}</p>
      <p class="product-price">{{ product_item.price }} $</p>
    </a>
    <div
      class="add-to-cart"
      :data-id="product_item.id"
      :data-name="product_item.name"
      :data-price="product_item.price"
      :data-imageUrl="product_item.imageUrl"
      @click="$emit('add-to-cart', product_item.id)"
    >
      <a class="add-to-cart-link link">
        <!--href="shopping-cart.html"-->
        <img
          class="small-cart"
          src="css/img/add-to-cart.svg"
          alt="add to cart"
        />
        Add to Cart
      </a>
    </div>
  </div>
</template>

<script>
export default {
  //   name: "Products",
  props: ["product_item"],
  components: {},
};
</script>