<template>
  <div class="slider-container">
    <div class="slider-elements">
      <button @click="prev" type="button" class="btn btn-left">
        <span class="alt-i alt-chevron-left"></span>
      </button>
      <div class="slider">
        <div
          class="container-slides"
          :style="{
            transform: `translateX(${index}px)`,
            transition: `${transition}`,
          }"
        >
          <img src="../img/fortnite.png" alt="" class="img-slider" />
          <img src="../img/webdesign.png" alt="" class="img-slider" />

          <img src="../img/apple_arcade.png" alt="" class="img-slider" />
        </div>
      </div>
      <button @click="next" type="button" class="btn btn-right">
        <span class="alt-i alt-chevron-right"></span>
      </button>
    </div>
    <div class="container-btn-slider">
      <div class="btn-slider selected"></div>
      <div class="btn-slider"></div>
      <div class="btn-slider"></div>
    </div>
    <text-category
      @changeText="textCategory = $event"
      :textCategory="update"
      :index="index"
    ></text-category>
  </div>
</template>

<script>
let btnSlider = document.getElementsByClassName("btn-slider");
let btnSelected = document.getElementsByClassName("selected");
import TextCategory from "./TextCategory.vue";

export default {
  name: "Slider",
  components: {
    "text-category": TextCategory,
  },
  props: {
    textCategory: String,
  },
  data: function () {
    return {
      index: 0,
      transition: "transform 0.3s ease",
    };
  },
  methods: {
    update(textCategory) {
      this.textCategory = textCategory;
    },
    next() {
      if (this.index === -1500) {
        this.transition = "none";
        this.index = 0;
        btnSlider[0].classList.add("selected");
        btnSelected[1].classList.remove("selected");
      } else {
        this.transition = "transform 0.2s ease";
        this.index -= 750;
        btnSelected[0].nextElementSibling.classList.add("selected");
        btnSelected[0].classList.remove("selected");
      }
    },
    prev() {
      if (this.index === 0) {
        btnSlider[2].classList.add("selected");
        btnSelected[0].classList.remove("selected");
        this.transition = "none";
        this.index = -1500;
      } else {
        this.transition = "transform 0.2s ease";
        this.index += 750;
        btnSelected[0].previousSibling.classList.add("selected");
        btnSelected[1].classList.remove("selected");
      }
    },
  },
};
</script>
