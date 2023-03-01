<template>
  <Layout>
    <Title />
    <div class="flex flex-row justify-evenly">
      <Card v-for="(elem, index) in data" :key="index" :data="elem" />
    </div>
  </Layout>
</template>

<script>
import Title from "~/components/Title";
import Card from "~/components/Card";
import Layout from "~/Layout";
import { DATA } from "~/constants";
export default {
  components: {
    Title,
    Card,
    Layout,
  },
  data() {
    return {
      data: DATA,
    };
  },
};
</script>
