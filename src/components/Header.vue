<template>
  <div>
    <header class="navbar" id="navbar">
      <div class="logo" @click="hideMenu">
        <a href="#hero">GoldieTattoo</a>
      </div>
      <div class="menu-btn">
        <button
          class="hamburger hamburger--spring"
          :class="{ active: isActive }"
          @click="toggleMenu"
        >
          <div class="hamburger-box">
            <div class="hamburger-inner"></div>
          </div>
        </button>
      </div>

      <v-burger-menu
        @click-on-menuLink="hideMenu"
        :class="{ opened: isOpened }"
      />
    </header>
  </div>
</template>

<script>
import BurgerMenu from "@/components/UI/BurgerMenu";
export default {
  el: "#navbar",
  components: {
    "v-burger-menu": BurgerMenu,
  },
  data() {
    return {
      isActive: false,
      isOpened: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isActive = !this.isActive;
      this.isOpened = !this.isOpened;
    },
    hideMenu() {
      this.isActive = false;
      this.isOpened = false;
    },
  },
};
</script>

<style scoped>
.navbar {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 40px;

  position: fixed;
  top: 0;
  left: 0;

  z-index: 1000;
}

.logo {
  margin-bottom: 25px;

  font-size: 46px;
  font-weight: 700;
  color: #fff;

  z-index: 10;
}

.menu-btn {
  z-index: 10;
}

.hamburger {
  padding: 15px 15px;
  display: inline-block;
  cursor: pointer;
  transition-property: opacity, filter;
  transition-duration: 0.15s;
  transition-timing-function: linear;
  font: inherit;
  color: inherit;
  text-transform: none;
  background-color: transparent;
  border: 0;
  margin: 0;
  overflow: visible;
}

.hamburger:hover {
  opacity: 0.8;
}

.hamburger.active .hamburger-inner,
.hamburger.active .hamburger-inner::before,
.hamburger.active .hamburger-inner::after {
  background-color: #fff;
}

.hamburger-box {
  width: 40px;
  height: 24px;
  display: inline-block;
  position: relative;
}

.hamburger-inner {
  display: block;
  top: 50%;
  margin-top: -2px;
}

.hamburger-inner,
.hamburger-inner::before,
.hamburger-inner::after {
  width: 40px;
  height: 3px;
  background-color: #fff;
  border-radius: 4px;
  position: absolute;
  transition-property: transform;
  transition-duration: 0.15s;
  transition-timing-function: ease;
}

.hamburger-inner::before,
.hamburger-inner::after {
  content: "";
  display: block;
}

.hamburger-inner::before {
  top: -10px;
}

.hamburger-inner::after {
  bottom: -10px;
}

/* Spring */
.hamburger--spring .hamburger-inner {
  top: 2px;
  transition: background-color 0s 0.13s linear;
}

.hamburger--spring .hamburger-inner::before {
  top: 10px;
  transition: top 0.1s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1),
    transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19);
}

.hamburger--spring .hamburger-inner::after {
  top: 20px;
  transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1),
    transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19);
}

.hamburger--spring.active .hamburger-inner {
  transition-delay: 0.22s;
  background-color: transparent !important;
}

.hamburger--spring.active .hamburger-inner::before {
  top: 0;
  transition: top 0.1s 0.15s cubic-bezier(0.33333, 0, 0.66667, 0.33333),
    transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1);
  transform: translate3d(0, 10px, 0) rotate(45deg);
}

.hamburger--spring.active .hamburger-inner::after {
  top: 0;
  transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333),
    transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1);
  transform: translate3d(0, 10px, 0) rotate(-45deg);
}

/*
   * Spring Reverse
   */
.hamburger--spring-r .hamburger-inner {
  top: auto;
  bottom: 0;
  transition-duration: 0.13s;
  transition-delay: 0s;
  transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
}

.hamburger--spring-r .hamburger-inner::after {
  top: -20px;
  transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1),
    opacity 0s linear;
}

.hamburger--spring-r .hamburger-inner::before {
  transition: top 0.1s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1),
    transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19);
}

.hamburger--spring-r.active .hamburger-inner {
  transform: translate3d(0, -10px, 0) rotate(-45deg);
  transition-delay: 0.22s;
  transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
}

.hamburger--spring-r.active .hamburger-inner::after {
  top: 0;
  opacity: 0;
  transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333),
    opacity 0s 0.22s linear;
}

.hamburger--spring-r.active .hamburger-inner::before {
  top: 0;
  transform: rotate(90deg);
  transition: top 0.1s 0.15s cubic-bezier(0.33333, 0, 0.66667, 0.33333),
    transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1);
}
</style>
