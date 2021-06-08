<template>
  <div class="p-5">
    <Title name="ADD" />
    <div class="flex">
      <input
        type="text"
        class="block w-3/4 focus:outline-none focus:border-green-500  border-gray-500 border rounded px-6 py-4"
      />
      <button
        class=" w-1/4 bg-gray-200 rounded-md ml-2 text-black hover:text-green-500 hover:bg-green-100 focus:outline-none"
      >
        登録
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import Title from "./Title.vue";
export default {
  name: "Add",
  components: {
    Title,
  },
};
</script>
