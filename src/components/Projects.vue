<template>
  <div class="projects">
    <div class="content">
      <div class="heading">
        The work I do, <br />
        and business I help.
      </div>

      <div class="project-list">
        <div class="item">
          <div class="image-container ridgeway">
            <img src="../assets/img/ridgeway.png" alt="" />
          </div>
          <h3>Rideway Realtors.</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
            repellendus impedit tempore pariatur deserunt possimus inventore!
            Dolor doloremque nobis quasi itaque, illum, ratione quam sunt
            voluptates nisi eius inventore eos.
          </p>
        </div>

        <div class="item">
          <div class="image-container erazerowaste">
            <img src="../assets/img/erazerowaste.png" alt="" />
          </div>
          <h3>EraZeroWaste.</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
            repellendus impedit tempore pariatur deserunt possimus inventore!
            Dolor doloremque nobis quasi itaque, illum, ratione quam sunt
            voluptates nisi eius inventore eos.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  name: "Projects",

  mounted() {
    function getWidth() {
      var box = document.querySelector(".image-container");
      var width = box.offsetWidth;

      console.log(width);

      $(".image-container").css("height", width + 30);
    }

    getWidth();
  },
};
</script>