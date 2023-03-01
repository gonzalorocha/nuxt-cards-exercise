<template>
  <div
    :style="{ width: canvasWidth + 'px', height: canvasHeight + 'px' }"
    :class="className"
  >
    <component
      :is="SvgIcon"
      :width="width"
      :height="height"
      aria-hidden="true"
      role="img"
      :focusable="false"
      v-bind="$rest"
    />
  </div>
</template>

<script>
import Arrow from "~/assets/icons/arrow.svg";
import Calendar from "~/assets/icons/calendar.svg";
import Location from "~/assets/icons/location.svg";

const SvgIcons = {
  Arrow,
  Calendar,
  Location,
};

export default {
  name: "Icon",

  props: {
    name: {
      type: String,
      required: true,
      validator: (value) => Object.keys(SvgIcons).includes(value),
    },
    className: String,
    width: {
      type: Number,
      default: 16,
    },
    height: {
      type: Number,
      default: 16,
    },
    canvasWidth: Number,
    canvasHeight: Number,
  },

  computed: {
    SvgIcon() {
      return SvgIcons[this.name];
    },
  },
};
</script>

<style scoped></style>
