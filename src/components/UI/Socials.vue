<template>
  <div class="socials">
    <a class="socials-item" href="#">
      <img
        class="socials-icon inst"
        src="../../assets/img/socials/insta.svg"
        alt="Instagram"
      />
    </a>
    <a class="socials-item" href="#">
      <img
        class="socials-icon vk"
        src="../../assets/img/socials/vk.svg"
        alt="Vkontakte"
      />
    </a>
    <a class="socials-item" href="#">
      <img
        class="socials-icon fb"
        src="../../assets/img/socials/fb.svg"
        alt="Facebook"
      />
    </a>
    <a class="socials-item" href="#">
      <img
        class="socials-icon tiktok"
        src="../../assets/img/socials/tiktok.svg"
        alt="Tiktok"
      />
    </a>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.socials {
  display: flex;
  justify-content: center;
  align-items: center;
}

.socials-item {
  margin-right: 5px;

  transition: all 0.3s ease;
}
.socials-item:last-child {
  margin-right: 0;
}
.socials-item:hover {
  transform: translateY(-5px);
}

.socials-icon {
  width: 35px;
  height: 35px;
  object-fit: cover;
}
.socials-icon.fb {
  width: 24px;
  height: 30px;
}
</style>
