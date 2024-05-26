<template>
  <div class="carousel-container">
    <div class="carousel" :style="{ transform: `translateX(-${currentSlide * 100}%)` }">
      <div class="carousel-slide" v-for="(image, index) in images" :key="index">
        <img :src="image" :alt="'Slide ' + (index + 1)">
      </div>
    </div>
    <button class="prev" @click="prevSlide">Prev</button>
    <button class="next" @click="nextSlide">Next</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentSlide: 0,
      images: [
        'https://i.pinimg.com/564x/fc/ba/e5/fcbae5e02653dba533d39dfd3b891a28.jpg',
        'https://i.pinimg.com/736x/6e/8e/3b/6e8e3b46ed9d7302adfedb411201008e.jpg',
        'https://i.pinimg.com/564x/8c/56/c9/8c56c917b74d8211327b7bc918644ee4.jpg'
      ],
    };
  },
  methods: {
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.images.length;
    },
    prevSlide() {
      this.currentSlide = (this.currentSlide - 1 + this.images.length) % this.images.length;
    }
  },
  mounted() {
    setInterval(this.nextSlide, 3000); // Auto slide every 3 seconds
  }
};
</script>

<style>
.carousel-container {
  position: relative;
  overflow: hidden;
  width: 100%;
  max-width: 600px;
  margin: auto;
}

.carousel {
  display: flex;
  transition: transform 0.5s ease;
}

.carousel-slide {
  min-width: 100%;
  box-sizing: border-box;
}

.carousel-slide img {
  width: 100%;
  display: block;
}

button.prev, button.next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}

button.prev {
  left: 10px;
}

button.next {
  right: 10px;
}
</style>
