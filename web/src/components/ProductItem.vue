<template>
  <div class="ProductItem">
    <img :src="product.image" alt="" />
    <h3>{{ product.title }}</h3>
    <p>{{ product.price }}</p>
    <a :href="`/products/${product.slug}`">details</a>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

interface Product {
  title: String;
  slug: String;
  image: String;
  price: Number;
}

@Component
export default class ProductItem extends Vue {
  product: Product;
}
</script>
