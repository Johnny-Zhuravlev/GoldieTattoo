<template>
  <div class="marketing">
    <div class="marketing-info-left">
      <div class="marketing-info-left-content">
        <h2 class="marketing-title">
          Команда лучших
          <br />
          тату-криэйторов
          <br />
          в Санкт-Петербурге
        </h2>
        <div class="marketing-subtitle">
          Берёмся за работы любой сложности.
          <br />
          Всегда проконсультируем и подскажем как лучше.
        </div>
        <Default-btn />
      </div>
    </div>
    <div class="marketing-info-right">
      <img
        class="marketing-img"
        src="../assets/img/marketing.jpg"
        alt="Тату-мастер Кристи делает контент для соцсетей"
      />
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
.marketing {
  display: flex;
  height: 100vh;
  min-height: 700px;
}

.marketing-info-right,
.marketing-info-left {
  width: 50%;
}
.marketing-info-left {
  display: flex;

  background: #000;
}
.marketing-info-left-content {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
}

.marketing-title {
  margin-bottom: 20px;

  font-size: 52px;
  line-height: 58px;
}

.marketing-subtitle {
  margin-bottom: 30px;

  font-size: 18px;
  line-height: 28px;
}

.marketing-img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
