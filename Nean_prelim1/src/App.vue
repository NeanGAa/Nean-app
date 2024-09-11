<template>
  <div id="app">
    <ItemList :products="products" />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue';

export default {
  name: 'App',
  components: {
    ItemList
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Product 1', price: 100 },
        { id: 2, name: 'Product 2', price: 200 },
        { id: 3, name: 'Product 3', price: 300 }
      ]
    };
  }
};
</script>