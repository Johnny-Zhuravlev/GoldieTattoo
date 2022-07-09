<template>
  <div class="preloader">
    <h2 class="preloader-logo">GoldieTattoo</h2>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.preloader {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;

  position: fixed;
  top: 0;
  left: 0;

  background: #000;

  animation: slideFade 1s 2.2s ease-in-out forwards;

  z-index: 10000;
}

.preloader-logo {
  overflow: hidden;

  font-size: 60px;
  line-height: 60px;
  color: #fbcf0a;

  position: relative;

  border-radius: 5px;
  transform: scale(0.75);
  opacity: 1;

  animation: zoom 1.5s ease-in-out forwards;
}

@keyframes zoom {
  0% {
    transform: scale(0.75);
  }
  100% {
    transform: scale(2);
  }
}

@keyframes slide {
  0% {
    transform: translateX(-101%);
  }
  100% {
    transform: scale(101%);
  }
}

@keyframes slideFade {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(101%) scaleX(0);
  }
}

.preloader-logo::before {
  width: 100%;
  height: 100%;
  content: "";

  position: absolute;
  top: 0;
  left: 0;

  background: radial-gradient(
    circle,
    rgba(255, 227, 103, 1) 0%,
    rgba(251, 207, 10, 1) 100%
  );
  transform: translateX(-101%);

  animation: slide 0.8s 1.5s linear forwards;
}
</style>
