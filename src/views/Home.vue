<template>
  <div class="home">
    <div class="cursor"></div>
    <Header />
    <Hero />
    <Technologies />
    <Projects />
  </div>
</template>

<script>
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
  },
};
</script>

