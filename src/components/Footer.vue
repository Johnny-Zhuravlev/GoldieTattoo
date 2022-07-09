<template>
  <div class="footer" id="footer">
    <iframe
      src="https://yandex.ru/map-widget/v1/?um=constructor%3A5a46dd91e75ef64d5d7a141558a8dfb3cbd83714ddcc8932a45b71e5bc3e895a&amp;source=constructor"
      width="100%"
      height="315"
      frameborder="0"
    ></iframe>

    <div class="footer-info">
      <ul class="contacts">
        <li class="contacts-item">Адрес: Кременчугская улица д.13к1 1этаж</li>
        <li class="contacts-item">
          <a href="tel:+78889900" class="contacts-link">
            Телефон для связи: +7-(888)-99-00
          </a>
        </li>
        <li class="contacts-item">
          <a href="mailto:napishimne@sladkiy.ru" class="contacts-link">
            napishimne@sladkiy.ru
          </a>
        </li>
      </ul>

      <div class="footer-socials">
        <h4 class="footer-socials-title">Мы в соцсетях:</h4>
        <Socials style="justify-content: flex-end" />
      </div>
    </div>

    <div class="footer-copyright">Created by JohnnyZ__Production</div>
  </div>
</template>

<script>
import Socials from "@/components/UI/Socials";
export default {
  components: {
    Socials,
  },
};
</script>

<style scoped>
.footer {
  padding: 135px 0 20px;

  background: #000;
}

.footer-info {
  display: flex;
  margin: 55px 0;
}

.contacts {
  width: 50%;
  margin: 0;
  padding: 0 0 0 5%;

  list-style: none;
}

.contacts-item {
  margin-bottom: 5px;
}

.contacts-link {
  text-decoration: none;
  color: inherit;
}

.footer-socials {
  width: 50%;
  padding-right: 5%;

  text-align: right;
}

.footer-socials-title {
  margin-bottom: 10px;
}

.footer-copyright {
  font-size: 13px;
  text-align: center;
}
</style>
