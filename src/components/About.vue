<template>
  <div class="about">
    <div class="about-content">
      <div class="about-content-text">
        <h2 class="about-title">
          Мы разработали интересные
          <br />
          курсы для тату-мастеров
          <br />
          разных уровней.
        </h2>
        <div class="about-subtitle">
          У развития нет определенной границы. Всё зависит исключительно от
          самого человека.
        </div>
        <div class="about-text">
          Нам не важно хочешь ли ты начать с самого нуля или уже что-то умеешь.
          А может ты уже хороший тату-артист, но хочешь расширить свои скилы.
          Если выберешь для себя одну из наших программ, то будь уверен(на), что
          ваш куратор расскажет все самое необходимое и выложится по полной.
        </div>
        <Default-btn></Default-btn>
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
.about-content {
  width: 100%;
  height: 100vh;
  min-height: 700px;

  background: url("../assets/img/AboutBg.jpg") 0 0 / cover no-repeat;

  position: relative;

  z-index: 1;
}

.about-content::before {
  content: "";
  width: 100%;
  height: 100%;

  background: #000;
  backdrop-filter: blur(2px);
  opacity: 0.7;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -1;
}

.about-content-text {
  width: 65%;
  height: auto;
  margin: 0 auto;
  padding: 0 0 175px 5%;

  position: absolute;
  bottom: 0;
  left: 0;
}

.about-title {
  margin-bottom: 15px;

  font-size: 52px;
  line-height: 56px;
}

.about-subtitle {
  margin-bottom: 15px;

  font-size: 20px;
  line-height: 24px;
}

.about-text {
  margin-bottom: 25px;

  font-size: 16px;
  line-height: 20px;
}
</style>
