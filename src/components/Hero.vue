<template>
  <div class="hero" id="hero">
    <div class="hero-video">
      <video
        class="hero-video-bg"
        poster="../assets/img/HeroPoster.jpg"
        muted
        loop
      >
        <source
          src="../assets/img/Moveton.mp4"
          type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'
        />
      </video>

      <div class="hero-content">
        <h1 class="hero-title">
          Творим чудеса на коже.
          <br />
          Рисуем, колим, красим.
          <br />
          Консультируем.
        </h1>

        <Default-btn />
      </div>
    </div>
  </div>
</template>

<script>
import DefaultBtn from "@/components/UI/DefaultBtn";
export default {
  components: {
    DefaultBtn,
  },
};
</script>

<style scoped>
.hero-video {
  width: 100%;
  height: 100vh;

  z-index: -1;
}
.hero-video::before {
  content: "";
  width: 100%;
  height: 100%;

  background: #000;
  backdrop-filter: blur(2px);
  opacity: 0.4;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -1;
}
.hero-video-bg {
  width: 100%;
  height: 100%;
  object-fit: cover;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -2;
}

.hero-content {
  width: 600px;
  height: auto;
  min-height: 150px;
  padding: 120px 5% 75px 0;

  text-align: right;

  position: absolute;
  bottom: 0;
  right: 0;
}

.hero-title {
  margin-bottom: 15px;

  font-size: 26px;
  line-height: 36px;
}
</style>
