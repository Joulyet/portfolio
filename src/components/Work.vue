<template>
  <section id="work">
    <h2  data-aos="fade-right" data-aos-delay="100"><span class="alt-i alt-computer"></span>Work</h2>
    <div  data-aos="fade-up" data-aos-delay="800" class="work-description">
    <p>
      I mainly work on development projects but sometimes I also work on more
      artistic projects, such as computer graphics, motion design or 3D.
    </p>
    <span>Find out more:</span>
    </div>
    <slider></slider>
  </section>
</template>

<script lang="ts">
import Slider from "./Slider.vue";

export default {
  name: "Work",
  components: {
    slider: Slider,
  },
};
</script>
