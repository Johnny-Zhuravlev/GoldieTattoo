<template>
  <div id="app">
    <Header />
    <Preloader />
    <Hero />
    <Marketing />
    <Workspace />
    <About />
    <Team />
    <Gallery />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Preloader from "@/components/UI/Preloader";
import Hero from "@/components/Hero";
import Marketing from "@/components/Marketing";
import Workspace from "@/components/Workspace";
import About from "@/components/About";
import Team from "@/components/Team";
import Gallery from "@/components/Gallery";
import Footer from "@/components/Footer";

export default {
  name: "App",
  components: {
    Header,
    Preloader,
    Hero,
    Marketing,
    Workspace,
    About,
    Team,
    Gallery,
    Footer,
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;

  font-family: "Helvetica", sans-serif;
  font-size: 16px;
  line-height: 24px;

  color: #fff;
  background-color: #000;
}

body::-webkit-scrollbar {
  width: 5px;
  display: none;
}
/* body::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
}
body::-webkit-scrollbar-thumb {
  background-color: #fd0202;
  outline: 1px solid slategrey;
} */

h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
  padding: 0;
}

a {
  color: inherit;
  text-decoration: none;
}
</style>
