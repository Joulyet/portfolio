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
    <skills></skills>
    <contact></contact>
  </main>
</template>

<script>
import About from "../components/About.vue";
import Work from "../components/Work.vue";
import Skills from "../components/Skills.vue";
import Contact from "../components/Contact.vue";

export default {
  name: "Home",
  components: {
    about: About,
    work: Work,
    skills: Skills,
    contact: Contact
  },
};
</script>
