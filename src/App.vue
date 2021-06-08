<template>
  <Layout>
    <div class="bg-white p-6">
      <img
        src="./assets/logo.png"
        alt="vue"
        class=" text-center m-auto"
        width="150"
        height="150"
      />
      <h1 class=" text-center text-green-500 text-5xl ">Vue TODO LIST</h1>
      <List :listData="listData" />
      <Add :listData="listData" />
    </div>
  </Layout>
</template>

<script lang="ts">
import Layout from "./components/Layout.vue";
import List from "./components/List.vue";
import Add from "./components/Add.vue";

type state = {
  listData: { id: number; name: string }[] | [];
};
export default {
  data(): state {
    return {
      listData: [
        {
          id: 1,
          name: "運動",
        },
        {
          id: 2,
          name: "勉強",
        },
      ],
    };
  },
  name: "App",
  components: {
    Layout,
    List,
    Add,
  },
};
</script>
