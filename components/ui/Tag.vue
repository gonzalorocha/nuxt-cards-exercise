<template>
  <div
    class="h-7 border border-blue rounded-lg flex justify-center items-center px-2"
  >
    <p class="text-blue uppercase text-2xs font-semibold">{{ name }}</p>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
  },
};
</script>
