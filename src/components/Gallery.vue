<template>
  <div class="gallery" id="gallery">
    <div class="gallery-content">
      <div class="gallery-item" v-for="work in works" :key="work.image">
        <img :src="work.image" alt="Фотография работы" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      works: [
        { image: require("@/assets/img/gallery/1.jpg") },
        { image: require("@/assets/img/gallery/2.jpg") },
        { image: require("@/assets/img/gallery/3.jpg") },
        { image: require("@/assets/img/gallery/4.jpg") },
        { image: require("@/assets/img/gallery/5.jpg") },
        { image: require("@/assets/img/gallery/6.jpg") },
        { image: require("@/assets/img/gallery/7.jpg") },
        { image: require("@/assets/img/gallery/8.jpg") },
        { image: require("@/assets/img/gallery/9.jpg") },
        { image: require("@/assets/img/gallery/10.jpg") },
        { image: require("@/assets/img/gallery/11.jpg") },
        { image: require("@/assets/img/gallery/12.jpg") },
        { image: require("@/assets/img/gallery/13.jpg") },
        { image: require("@/assets/img/gallery/14.jpg") },
        { image: require("@/assets/img/gallery/15.jpg") },
        { image: require("@/assets/img/gallery/16.jpg") },
      ],
    };
  },
};
</script>

<style scoped>
.gallery {
  padding: 125px 60px 100px;

  background: #000;
}
.gallery-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 450px 450px 450px;
  gap: 15px;
}

.gallery-item {
  box-shadow: 0 0 3px 3px rgba(255, 255, 255, 0.2);
}

.gallery-item img {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
}
</style>
