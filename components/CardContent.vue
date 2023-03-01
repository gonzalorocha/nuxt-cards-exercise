<template>
  <div>
    <div class="flex flex-row gap-2 text-gray-500 text-md">
      <Icon name="Location" />
      {{ location }}
    </div>
    <div class="flex flex-row gap-2 text-gray-500 text-md mt-3">
      <Icon name="Calendar" />
      <Date :date="date" />
    </div>
    <div class="flex flex-row gap-1 mt-3">
      <Tag v-for="tag in tags" :key="tag" :name="tag" />
    </div>
  </div>
</template>

<script>
import Icon from "~/components/ui/Icon";
import Tag from "~/components/ui/Tag";
import Date from "~/components/ui/Date";

export default {
  props: {
    location: {
      type: String,
      required: true,
    },
    date: {
      type: [String, Number, Date],
      required: true,
    },
    tags: {
      type: Array,
      default: () => [],
    },
  },
  components: {
    Icon,
    Tag,
    Date,
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>
