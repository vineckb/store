<template>
  <div class="home">
    <ProductItem
      v-for="product in products"
      :product="product"
      :key="product.id"
    />
  </div>
</template>

<script>
import ProductItem from "@/components/ProductItem";

export default {
  components: { ProductItem },

  data() {
    return {
      products: [
        {
          id: 1,
          title: "title...",
          slug: "slug",
          price: 10,
          image: "http://...",
        },
      ],
    };
  },
};
</script>
