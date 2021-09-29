<template>
  <header class="header">
    <div class="container header-box">
      <div class="header-left">
        <a class="logo" href="index.html">
          <img src="css/img/logo.svg" alt="logo" />
          <p class="brand">Bran<span class="brand-d pink">d</span></p>
        </a>
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
                  <a href="product.html" class="mega-link link"
                    >Sweaters/Knits</a
                  >
                </li>
                <li>
                  <a href="product.html" class="mega-link link"
                    >Jackets/Coats</a
                  >
                </li>
                <li>
                  <a href="product.html" class="mega-link link">Blazers</a>
                </li>
                <li><a href="product.html" class="mega-link link">Demin</a></li>
                <li>
                  <a href="product.html" class="mega-link link"
                    >Leggings/Pants</a
                  >
                </li>
                <li>
                  <a href="product.html" class="mega-link link"
                    >Skirts/Shorts</a
                  >
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
                  <a href="product.html" class="mega-link link"
                    >Tees/Tank tops</a
                  >
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
                  <a href="product.html" class="mega-link link"
                    >Jackets/Vests</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </details>
        <form action="#" class="header-form">
          <input
            class="input-text"
            type="text"
            placeholder="Search for Item..."
          />
          <button type="submit" class="fa-search"></button>
        </form>
      </div>
      <div class="header-right">
        <Cart v-bind:cart="cart" @remove-from-cart="remove" />
        <details class="details-my-account">
          <summary class="button my-account">My account</summary>
          <div class="my-account-menu"></div>
        </details>
      </div>
    </div>
  </header>
</template>

<script>
import Cart from "@/components/Cart";

export default {
  name: "Header",
  props: ["cart"],
  data() {
    return {
      // cart: [],
    };
  },
  components: {
    Cart,
  },
  methods: {
    // !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!МНЕ КАЖЕТСЯ, ЧТО ДОБАВЛЕНИЕ ТОВАРА В КОРЗИНУ ДОЛЖНО ПРОИСХОДИТЬ В КОМПОНЕНТЕ КОРЗИНЫ, НО Я НЕ ПОНЯЛА, КАК ЭТО СДЕЛАТЬ
    // add(id) {
    //   let a = this.cart.findIndex((item) => item.id === id);
    //   if (a != -1) {
    //     this.cart[a].count++;
    //   } else {
    //     this.cart.push(this.products[id]);
    //     this.cart[this.cart.length - 1].count = 1;
    //   }
    // },
    // !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!ТОТ ЖЕ ВОПРОС И ПРО УДАЛЕНИЕ
    // remove(id) {
    //   let indx = this.cart.findIndex((item) => item.id == id);
    //   if (indx != -1) {
    //     this.cart.splice(indx, 1);
    //   }
    //   console.log("privet");
    // },
  },
};
</script>