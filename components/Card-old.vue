<template>
  <div :class="[$style.card, className]">
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

<style scoped>
.card {
  width: 310px;
  height: 550px;
  background-color: white;
  border-radius: 20px;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
}
</style>
