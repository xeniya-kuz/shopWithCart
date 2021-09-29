<template>
  <figure class="my-account-item">
    <img
      class="my-account-item_size"
      :src="cart_item.imageUrl"
      :alt="cart_item.name"
    />
    <div class="my-acc-right">
      <div class="my-acc-info">
        <h3 class="my-acc-head">{{ cart_item.name }}</h3>
        <div class="review_stars stars-height">
          <input id="star6-5" type="radio" name="stars" />
          <label title="Отлично" for="star6-5">
            <i class="fas fa-star"></i>
          </label>
          <input id="star6-4" type="radio" name="stars" />
          <label title="Хорошо" for="star6-4">
            <i class="fas fa-star"></i>
          </label>
          <input id="star6-3" type="radio" name="stars" />
          <label title="Нормально" for="star6-3">
            <i class="fas fa-star"></i>
          </label>
          <input id="star6-2" type="radio" name="stars" />
          <label title="Плохо" for="star6-2">
            <i class="fas fa-star"></i>
          </label>
          <input id="star6-1" type="radio" name="stars" />
          <label title="Ужасно" for="star6-1">
            <i class="fas fa-star"></i>
          </label>
        </div>
        <div class="my-acc-text">
          <span class="product-count" :data-id="id">{{ cart_item.count }}</span
          ><span class="text-x">x</span>${{ cart_item.price }}
        </div>
      </div>
      <a
        class="fas fa-times-circle"
        :data-id="cart_item.id"
        href="#"
        @click="$emit('remove-from-cart', cart_item.id)"
      ></a>
    </div>
  </figure>
</template>

<script>
export default {
  name: "Cart",
  props: ["cart_item"],
  data() {
    return {
      //   cart: [],
    };
  },
};
</script>

 