<template>
  <div class="container product-box">
    <ProductItem
      v-for="item of products"
      :key="item.id"
      v-bind:product_item="item"
      @add-to-cart="add"
    />
  </div>
</template>

<script>
import ProductItem from "@/components/ProductItem";

export default {
  name: "Products",
  props: ["products"],
  components: {
    ProductItem,
  },
  methods: {
    add(id) {
      this.$emit("add-to-cart", id);
    },
  },
};
</script>