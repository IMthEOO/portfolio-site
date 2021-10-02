<template>
  <div class="hero">
    <div class="content">
      <div class="hero-img">
        <img alt="logo" src="../assets/img/logo.png" />
      </div>
      <div class="welcome">Hi, I’m Osose</div>
      <div class="hero-intro">
        Building beautiful websites & creating great experiences.
      </div>
      <div class="hero-intro-p">
        A professional web developer and an imaginative front-end develper, who
        also loves no-code technology.
      </div>
      <div class="hero-connect-btn">
        <button>Connect with me</button>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  name: "Hero",

  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    let tl = gsap.timeline({
      // yes, we can add it to an entire timeline!
      scrollTrigger: {
        trigger: ".hero",
        start: "top top-=-100px", // when the top of the trigger hits the top of the viewport
        end: "+=500", // end after scrolling 500px beyond the start
      },
    });

    tl.from(".hero-intro", {
      scale: 0.5,
      opacity: 0,
      duration: 1,
      autoAlpha: 0,
    }).from(
      ".hero-connect-btn button",
      {
        opacity: 0,
        autoAlpha: 0,
        duration: 1,
      },
      "-=1"
    );
  },
};
</script>