<template>
  <Layout>
    <div class="bg-white p-6">
      <img src="./assets/logo.png" alt="vue" class=" text-center m-auto" width="150" height="150">
      <h1 class=" text-center text-green-500 text-5xl ">Vue TODO LIST</h1>
      <Title name="LIST"/>
      <Title name="ADD"/>
    </div>
  </Layout>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Layout from "./components/Layout.vue"
import Title from "./components/Title.vue"
@Options({
  components: {
    Layout,
    Title
  },
})
export default class App extends Vue {}
</script>


