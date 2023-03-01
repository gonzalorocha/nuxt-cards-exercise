<template>
  <div :class="[className, 'h-32']">
    <p class="mb-1 text-md font-semibold text-gray-300 uppercase">
      {{ category }}
    </p>
    <h1 class="text-xl font-bold">{{ text }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    category: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    className: String,
  },
};
</script>
