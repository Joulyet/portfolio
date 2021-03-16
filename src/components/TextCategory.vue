<template>
  <p id="text-category" class="test" v-on="changeCategory()">
    {{ textCategory }}
  </p>
</template>

<script>
export default {
  props: {
    textCategory: {
      default: "Web development",
    },
    index: {
      default: 0,
    },
  },

  methods: {
    changeCategory() {
      switch (this.index) {
        case 0:
          this.textCategory = "Web development";
          break;
        case -750:
          this.textCategory = "Web design";
          break;
        case -1500:
          this.textCategory = "Graphic design";
          break;
      }
      this.$emit("changeText", this.textCategory);
    },
  },
};
</script>
