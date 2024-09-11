
<template>
  <div v-if="isVisible">
    <h2>{{ product.name }}</h2>
    <p>Price: {{ product.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    product: Object
  },
  data() {
    return {
      isVisible: true 
    };
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product);
    }
  }
};
</script>