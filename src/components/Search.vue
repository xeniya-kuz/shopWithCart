<template>
  <details class="details-browse">
    <summary class="browse">Browse</summary>
    <div class="mega-menu mega-menu-browse">
      <div class="mega-item">
        <p class="mega-head">Women</p>
        <ul class="mega-list">
          <li>
            <a href="product.html" class="mega-link link">Dresses</a>
          </li>
          <li><a href="product.html" class="mega-link link">Tops</a></li>
          <li>
            <a href="product.html" class="mega-link link">Sweaters/Knits</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Jackets/Coats</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Blazers</a>
          </li>
          <li><a href="product.html" class="mega-link link">Demin</a></li>
          <li>
            <a href="product.html" class="mega-link link">Leggings/Pants</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Skirts/Shorts</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Accessories</a>
          </li>
        </ul>
      </div>
      <div class="mega-item">
        <p class="mega-head">Men</p>
        <ul class="mega-list">
          <li>
            <a href="product.html" class="mega-link link">Tees/Tank tops</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Shirts/Polos</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Sweaters</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link"
              >Sweatshirts/Hoodies</a
            >
          </li>
          <li>
            <a href="product.html" class="mega-link link">Blazers</a>
          </li>
          <li>
            <a href="product.html" class="mega-link link">Jackets/Vests</a>
          </li>
        </ul>
      </div>
    </div>
  </details>
  <form
    action="#"
    class="header-form"
    @submit.prevent="$root.$refs.products.filter(searchLine)"
  >
    <input
      class="input-text"
      type="text"
      placeholder="Search for Item..."
      v-model="searchLine"
    />
    <button type="submit" class="fa-search"></button>
  </form>
</template>
<script>
export default {
  props: ["products"],
  data() {
    return {
      searchLine: "",
    };
  },
  methods: {
    filterProducts(searchLine) {
      return searchLine;
    },
  },
};
</script>