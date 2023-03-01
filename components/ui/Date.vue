<template>
  <p :class="className">{{ formatDate(date) }}</p>
</template>

<script>
import { formatDate } from "~/utils/formatter";

export default {
  name: "Date",
  props: {
    date: {
      type: [String, Number, Date],
      required: true,
    },
    className: {
      type: String,
      default: "",
    },
  },
  methods: {
    formatDate(date) {
      return formatDate(date);
    },
  },
};
</script>
