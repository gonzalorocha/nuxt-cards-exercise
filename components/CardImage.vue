<template>
  <div
    class="w-full h-[250px] duration-300 bg-cover bg-position-center bg-no-repeat z-0"
  >
    <img :src="imageSrc" alt="" />
  </div>
</template>

<script>
import choco from "~/assets/choco.png";
import excursion from "~/assets/excursion.png";
import panoramic from "~/assets/panoramic.png";

export default {
  name: "CardImage",
  props: {
    imageName: {
      type: String,
      required: true,
    },
  },
  computed: {
    imageSrc() {
      switch (this.imageName) {
        case "choco":
          return choco;
        case "excursion":
          return excursion;
        default:
          return panoramic;
      }
    },
  },
};
</script>

<style>
/* styles go here */
</style>
