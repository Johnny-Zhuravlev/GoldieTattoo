<template>
  <ul class="burger-menu" id="burger-menu" :class="{ opened: isOpened }">
    <li v-for="link in links" :key="link.id" class="burger-menu-item">
      <a
        class="burger-menu-link"
        :href="link.href"
        @click="$emit('click-on-menuLink')"
      >
        {{ link.name }}
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  el: "#burger-menu",
  data() {
    return {
      links: [
        { id: 1, name: "Галерея", href: "#gallery" },
        { id: 2, name: "Команда", href: "#team" },
        { id: 3, name: "Контакты", href: "#footer" },
      ],
      isOpened: false,
    };
  },
};
</script>

<style scoped>
.burger-menu {
  width: 100%;
  margin: 0;
  padding: 155px 0 30px;

  text-align: center;

  background: #000;
  list-style: none;

  transition: all 0.3s ease-in;

  position: absolute;
  top: -340px;
}
.burger-menu.opened {
  top: 0;
}

.burger-menu-item {
  width: 150px;
  padding: 5px 0;
  margin: 0 auto;

  font-size: 20px;
  line-height: 28px;
  text-transform: uppercase;

  cursor: pointer;

  transition: all 0.2s ease;
}
.burger-menu-item:hover {
  color: #fbcf0a;
}

.burger-menu-link {
  color: inherit;
  text-decoration: none;
}
</style>
