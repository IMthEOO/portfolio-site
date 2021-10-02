<template>
  <div class="home">
    <div class="cursor"></div>
    <Header />
    <Hero />
    <Technologies />
    <Projects />

    <div class="theme-toggle">
      <div class="toggle-track"></div>
      <div class="toggle-thumb"></div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import Technologies from "@/components/Technologies.vue";
import Projects from "@/components/Projects.vue";

export default {
  name: "Home",
  components: {
    Header,
    Hero,
    Technologies,
    Projects,
  },
  mounted() {
    const cursor = document.querySelector(".cursor");

    document.addEventListener("mousemove", (e) => {
      cursor.setAttribute(
        "style",
        "top: " + (e.pageY - 10) + "px; left: " + (e.pageX - 10) + "px;"
      );
    });

    document.addEventListener("click", () => {
      cursor.classList.add("expand");

      setTimeout(() => {
        cursor.classList.remove("expand");
      }, 500);
    });

    $(".toggle-thumb").click(() => {
      $("body").toggleClass("dark");
      $(".theme-toggle").toggleClass("active");
    });
  },
};
</script>

