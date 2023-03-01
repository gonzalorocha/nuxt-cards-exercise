<template>
  <div class="w-[310px] h-[550px] bg-white rounded-xl shadow-md">
    <CardImage :imageName="data.imageName" />
    <div class="px-7 pt-2 h-full flex flex-col justify-between">
      <CardTitle :category="data.category" :text="data.title" />
      <CardContent
        :location="data.location"
        :date="data.date"
        :tags="data.tags"
      />
      <Button
        class="mb-6 mt-4"
        text="ver más"
        @click="() => alert(data.title)"
      />
    </div>
  </div>
</template>

<script>
import CardImage from "./CardImage";
import CardTitle from "./CardTitle";
import CardContent from "./CardContent";
import Button from "./ui/Button";

export default {
  props: {
    data: {
      type: Object,
      required: true,
    },
    className: {
      type: String,
      default: "",
    },
  },
  components: {
    CardImage,
    CardTitle,
    CardContent,
    Button,
  },
};
</script>

<style scoped></style>
