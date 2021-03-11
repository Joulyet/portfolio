<template>
  <main>
    <section id="home">
      <div id="home-text">
        <span class="line-title-1">Hello, welcome</span>
        <span class="line-title-2">My name is <b>Juliet Patron</b></span>
        <span class="line-title-3"
          >Front-end <b>developer</b> and <b>student</b></span
        >
      </div>
    </section>
    <about></about>
    <work></work>
  </main>
</template>

<script>

import About from "../components/About.vue";
import Work from "../components/Work.vue";

export default {
  name: "Home",
  components: {
    "about": About,
    "work": Work,
  },
};

</script>