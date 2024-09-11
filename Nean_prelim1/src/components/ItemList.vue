  <template>
  <div>
    <h1>Product List</h1>
    <div v-for="item in filteredItems" :key="item.id">
      <Item :product="item" @add-to-cart="handleAddToCart" />
    </div>
  </div>
</template>

<script>
import Item from './Item.vue';

export default {
  name: 'ItemList',
  components: {
    Item
  },
  props: {
    products: Array
  },
  data() {
    return {
      isVisible: true, 
    };
  },
  computed: {
    filteredItems() {
      
      return this.isVisible ? this.products : [];
    }
  },
  methods: {
    handleAddToCart(product) {
      console.log('${product.name}added to cart at price ${product.price}');
    }
  }
};
</script>
