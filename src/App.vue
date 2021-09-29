<template>
  <!-- <Header v-bind:cart="cart" />-->
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
        <form action="#" class="header-form" @submit.prevent="filter">
          <!-- $root.$refs.products.filterProducts(searchLine) -->
          <input
            class="input-text"
            type="text"
            placeholder="Search for Item..."
            v-model="searchLine"
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

  <nav class="navigation">
    <div class="container">
      <ul class="menu">
        <li class="menu-list">
          <a href="product.html" class="menu-link">Home</a>
          <div class="mega-menu mega-menu-position">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list">
          <a href="product.html" class="menu-link">Man</a>
          <div class="mega-menu mega-menu-position">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list product-menu">
          <a href="product.html" class="menu-link">Women</a>
          <div class="mega-menu mega-menu-position">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list">
          <a href="product.html" class="menu-link">Kids</a>
          <div class="mega-menu mega-menu-position">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list">
          <a href="product.html" class="menu-link">Accoseriese</a>
          <div class="mega-menu mega-menu-position mega-reverse">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list">
          <a href="product.html" class="menu-link">Featured</a>
          <div class="mega-menu mega-menu-position mega-reverse">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
        <li class="menu-list">
          <a href="product.html" class="menu-link">Hot deals</a>
          <div class="mega-menu mega-menu-position mega-reverse">
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
              </ul>
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
              </ul>
            </div>
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
              </ul>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </nav>
  <div class="banner-top">
    <div class="container banner-top-box">
      <div class="banner-top-text">
        <p class="the-brand">The brand</p>
        <p class="luxerious">
          of luxerious
          <span class="pink">fashion</span>
        </p>
      </div>
    </div>
  </div>
  <div class="hot-deals-box container">
    <div class="hot-deals-left">
      <a class="for-men hot-deals-img" href="product.html">
        <div class="hot-deals-text">
          <p class="hot-deals-text-black">Hot deal</p>
          <p class="hot-deals-text-pink">For men</p>
        </div>
      </a>
      <a class="accesories hot-deals-img" href="product.html">
        <div class="hot-deals-text">
          <p class="hot-deals-text-black">Luxirous &amp; trendy</p>
          <p class="hot-deals-text-pink">Accesories</p>
        </div>
      </a>
    </div>
    <div class="hot-deals-right">
      <a class="for-women hot-deals-img" href="product.html">
        <div class="hot-deals-text">
          <p class="hot-deals-text-black">30% offer</p>
          <p class="hot-deals-text-pink">Women</p>
        </div>
      </a>
      <a class="for-kids hot-deals-img" href="product.html">
        <div class="hot-deals-text">
          <p class="hot-deals-text-black">New arrivals</p>
          <p class="hot-deals-text-pink">For kids</p>
        </div>
      </a>
    </div>
  </div>
  <section>
    <div class="container text-box">
      <h3>Fetured Items</h3>
      <p class="shop-for">
        Shop for items based on what we featured in this week
      </p>
    </div>
    <!-- <div class="container product-box">
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product1.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product2.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product3.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product4.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product5.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product6.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product7.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
            <div class="item">
                <a href="single-page.html" class="product-card">
                    <img class="product-img" src="img/product8.jpeg" alt="product">
                    <p class="product-text">Mango people t-shirt</p>
                    <p class="product-price">$52.00</p>
                </a>
                <div class="add-to-cart">
                    <a class="add-to-cart-link link" href="shopping-cart.html">
                        <img class="small-cart" src="img/add-to-cart.svg" alt="add to cart">
                        Add to Cart
                    </a>
                </div>
            </div>
        </div> -->
    <!-- 
        <div class="container product-box">
        </div> -->

    <main>
      <!-- <products ref="products"></products> -->
      <Products v-bind:products="products" @add-to-cart="add" />
      <!-- <error ref="error"></error> -->
    </main>
  </section>
  <!-- fas fa-long-arrow-alt-right -->
  <div class="browse-all-position">
    <a class="button browse-all" href="product.html">Browse All Product</a>
  </div>
  <div class="banner-bottom container">
    <a class="banner-bottom-link" href="product.html">
      <div class="banner-bottom-left">
        <div class="banner-bottom-left-text">
          <p class="percent">30% <span class="pink">offer</span></p>
          <p class="banner-women">for women</p>
        </div>
      </div>
      <div class="banner-bottom-right">
        <header class="advantages-index block-1">
          <img class="delivery" src="css/img/delivery.svg" alt="delivery" />
          <section class="advantages-block">
            <h3 class="advantages-head">Free Delivery</h3>
            <p class="advantages-article">
              Worldwide delivery on all. Authorittively morph next-generation
              innovtion with extensive models.
            </p>
          </section>
        </header>
        <header class="advantages-index block-2">
          <img class="sales" src="css/img/sales.svg" alt="sales" />
          <section class="advantages-block">
            <h3 class="advantages-head">Sales & discounts</h3>
            <p class="advantages-article">
              Worldwide delivery on all. Authorittively morph next-generation
              innovtion with extensive models.
            </p>
          </section>
        </header>
        <header class="advantages-index block-3">
          <img class="quality" src="css/img/quality.svg" alt="quality" />
          <section class="advantages-block">
            <h3 class="advantages-head">Quality assurance</h3>
            <p class="advantages-article">
              Worldwide delivery on all. Authorittively morph next-generation
              innovtion with extensive models.
            </p>
          </section>
        </header>
      </div>
    </a>
  </div>
  <footer class="footer">
    <div class="feedback-block">
      <div class="feedback-container container">
        <figure class="feedback-figure">
          <img class="feedback-img" src="css/img/face.png" alt="feedback" />
          <div class="feedback-all-text">
            <div class="feedback-text">
              “Vestibulum quis porttitor dui! Quisque viverra nunc mi, a
              pulvinar purus condimentum a. Aliquam condimentum mattis neque sed
              pretium”
            </div>
            <div class="feedback-name">Bin Burhan</div>
            <div class="feedback-place">Dhaka, Bd</div>
            <div class="slide-box">
              <div class="slide-part"></div>
              <div class="slide-part"></div>
              <div class="slide-part"></div>
            </div>
          </div>
        </figure>
        <div class="br"></div>
        <div class="subscribe">
          <div class="subscribe-text">
            <div class="subscribe-head">
              Subscribe
              <div class="subscribe-article">
                FOR OUR NEWLETTER AND PROMOTION
              </div>
            </div>
          </div>
          <form class="subscribe-form" action="#">
            <input
              class="input-subscribe"
              type="email"
              name="simple"
              placeholder="Enter Your Email"
            />
            <button class="subscribe-button button" type="submit">
              Subscribe
            </button>
          </form>
        </div>
      </div>
    </div>
    <div class="footer-text container">
      <div class="footer-text-left">
        <a class="logo" href="index.html">
          <img src="css/img/logo.svg" alt="logo" />
          <p class="brand">Bran<span class="brand-d pink">d</span></p>
        </a>
        <div class="footer-text-left-article">
          Objectively transition extensive data rather than cross functional
          solutions. Monotonectally syndicate multidisciplinary materials before
          go forward benefits. Intrinsicly syndicate an expanded array of
          processes and cross-unit partnerships.

          <p class="indent">
            Efficiently plagiarize 24/365 action items and focused
            infomediaries. Distinctively seize superior initiatives for wireless
            technologies. Dynamically optimize.
          </p>

          <p class="indent">
            Objectively strategize seamless relationships via resource sucking
            testing procedures. Proactively cultivate next-generation results
            for value-added methodologies. Dynamically plagiarize unique
            methodologies after performance based methodologies. Monotonectally
            empower stand-alone mindshare rather than ubiquitous opportunities.
            Dynamically orchestrate resource sucking scenarios after alternative
            synergy.
          </p>

          <p class="indent">
            Compellingly envisioneer corporate methods of empowerment before
            standards compliant technologies. Objectively facilitate
            progressive.
          </p>
        </div>
      </div>
      <div class="footer-text-right">
        <div>
          <div class="map-head pink">Company</div>
          <ul class="map-list">
            <li><a class="map-link link" href="index.html">Home</a></li>
            <li><a class="map-link link" href="product.html">Shop</a></li>
            <li><a class="map-link link" href="#">About</a></li>
            <li><a class="map-link link" href="#">How It Works</a></li>
            <li><a class="map-link link" href="#">Contact</a></li>
          </ul>
        </div>
        <div class="map">
          <div class="map-head pink">Information</div>
          <ul class="map-list">
            <li><a class="map-link link" href="#">Terms & Condition</a></li>
            <li><a class="map-link link" href="#">Privacy Policy</a></li>
            <li><a class="map-link link" href="#">How to Buy</a></li>
            <li><a class="map-link link" href="#">How to Sell</a></li>
            <li><a class="map-link link" href="#">Promotion</a></li>
          </ul>
        </div>
        <div class="map">
          <div class="map-head pink">Shop Category</div>
          <ul class="map-list">
            <li><a class="map-link link" href="product.html">Men</a></li>
            <li><a class="map-link link" href="product.html">Women</a></li>
            <li><a class="map-link link" href="product.html">Child</a></li>
            <li><a class="map-link link" href="#">Apparel</a></li>
            <li><a class="map-link link" href="product.html">Brows All</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container flex">
        <div class="footer-bottom-copy">
          &copy; 2021 Brand All Rights Reserved.
        </div>
        <div class="footer-bottom-social">
          <ul>
            <li class="icon">
              <a class="social fa-facebook" href="#"></a>
            </li>
            <li class="icon">
              <a class="social fa-twitter" href="#"></a>
            </li>
            <li class="icon">
              <a class="social fa-linkedin-in" href="#"></a>
            </li>
            <li class="icon">
              <a class="social fa-pinterest-p" href="#"></a>
            </li>
            <li class="icon">
              <a class="social fa-google-plus-g" href="#"></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
  <!-- <script src="script.js"></script> -->
</template>

<script>
import Products from "@/components/Products";
import Cart from "@/components/Cart";
// import Search from "@/components/Search";
// import Header from "@/components/Header";

export default {
  name: "App",
  data() {
    return {
      products: [
        {
          id: 0,
          name: "T-shirt",
          price: 300,
          imageUrl: "css/img/product1.jpeg",
        },
        {
          id: 1,
          name: "Blouse",
          price: 250,
          imageUrl: "css/img/product2.jpeg",
        },
        {
          id: 2,
          name: "Jacket",
          price: 450,
          imageUrl: "css/img/product3.jpeg",
        },
        {
          id: 3,
          name: "Blouse",
          price: 120,
          imageUrl: "css/img/product4.jpeg",
        },
        {
          id: 4,
          name: "Blouse",
          price: 270,
          imageUrl: "css/img/product5.jpeg",
        },
        {
          id: 5,
          name: "Jacket",
          price: 500,
          imageUrl: "css/img/product6.jpeg",
        },
        {
          id: 6,
          name: "Trousers",
          price: 430,
          imageUrl: "css/img/product7.jpeg",
        },
        {
          id: 7,
          name: "Shorts",
          price: 350,
          imageUrl: "css/img/product8.jpeg",
        },
      ],
      cart: [],
      filtered: [],
      searchLine: "",
    };
  },
  components: {
    Products,
    Cart,
    // Search,
    // Header,
  },
  methods: {
    // !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!МНЕ КАЖЕТСЯ, ЧТО ДОБАВЛЕНИЕ ТОВАРА В КОРЗИНУ ДОЛЖНО ПРОИСХОДИТЬ В КОМПОНЕНТЕ КОРЗИНЫ, НО Я НЕ ПОНЯЛА, КАК ЭТО СДЕЛАТЬ
    add(id) {
      let a = this.cart.findIndex((item) => item.id === id);
      if (a != -1) {
        this.cart[a].count++;
      } else {
        this.cart.push(this.products[id]);
        this.cart[this.cart.length - 1].count = 1;
      }
    },

    // !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!ТОТ ЖЕ ВОПРОС И ПРО УДАЛЕНИЕ
    remove(id) {
      let indx = this.cart.findIndex((item) => item.id == id);
      if (indx != -1) {
        this.cart.splice(indx, 1);
      }
    },
  },

  // !!!!!!!!!!!!!!!!!!!!!ПОЧЕМУ НЕ РАБОТАЕТ? НЕ ПОЛУЧИЛОСЬ СДЕЛАТЬ ПОИСК
  filter() {
    console.log(this.searchLine);
    // const regexp = new RegExp(value, "i");
    // this.filtered = this.products.filter((product) =>
    //   regexp.test(product.name)
    // );
  },
};
</script>

<style>
/* #app {
} */
</style>
