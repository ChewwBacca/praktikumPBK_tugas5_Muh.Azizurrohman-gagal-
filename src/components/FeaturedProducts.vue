<template>
  <section class="featured-products">
    <h2>New Products</h2>
    <div class="products">
      <div class="product" v-for="product in products" :key="product.id">
        <img :src="product.image" :alt="product.name" />
        <h3>{{ product.name }}</h3>
        <p class="price">{{ product.price }}</p>
        <p class="description">{{ product.description }}</p>
        <button @click="addToCart(product)">Add to Cart</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeaturedProducts',
  data() {
    return {
      products: [
        { id: 1, name: 'Product 1', price: 'Rp.40.000.000', image: 'https://i.pinimg.com/564x/7c/35/0c/7c350c553f29df7acddc37b62e708ff5.jpg', description: 'Laptop with the latest graphics card and high refresh rate screen for an immersive gaming experience. No more lag or frame drops!' },
        { id: 2, name: 'Product 2', price: 'Rp.24.000.000', image: 'https://i.pinimg.com/originals/c9/85/97/c9859714f6d488ec3b7a3489e9294d99.jpg', description: 'This laptop comes with an elegant design and high quality materials. Equipped with security features and great battery life.' },
        { id: 3, name: 'Product 3', price: 'Rp.32.000.000', image: 'https://i.pinimg.com/564x/d2/30/e7/d230e7f0bd6ca83fe5df5dc6f552dab4.jpg', description: 'Enjoy speed and efficiency with the latest processors and large storage capacities. Perfect for multitasking and unlimited creativity.' }
      ]
    };
  },
  methods: {
    addToCart(product) {
      console.log('Adding to cart:', product);
      // Implement the actual add to cart functionality here
    }
  }
};
</script>

<style scoped>
.featured-products {
  padding: 50px 20px;
  background-color: #f9f9f9;
}

.featured-products h2 {
  margin-bottom: 20px;
  color: black;
}

.products {
  display: flex;
  justify-content: space-around;
}

.product {
  background-color: white;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.product img {
  max-width: 100%;
  height: auto;
}

.product h3 {
  margin: 10px 0;
}

.product .price {
  color: #ff6600;
  font-size: 1.2em;
  margin: 0;
}

.product .description {
  color: #555;
  margin-top: 10px;
}

.product button {
  margin-top: 15px;
  padding: 10px 20px;
  background-color: #ff6600;
  color: white;
  border: none;
  cursor: pointer;
  font-size: 1em;
  transition: background-color 0.3s;
}

.product button:hover {
  background-color: #cc5200;
}
</style>
