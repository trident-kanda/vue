<template>
  <div class="p-5">
    <Title name="ADD" />
    <div class="flex">
      <input
        v-model="name"
        type="text"
        class="block w-3/4 focus:outline-none focus:border-green-500  border-gray-500 border rounded px-6 py-4"
      />
      <button
        class=" w-1/4 bg-gray-200 rounded-md ml-2 text-black hover:text-green-500 hover:bg-green-100 focus:outline-none"
        v-on:click="addList(listData, name)"
      >
        登録
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import Title from "./Title.vue";
import { PropType } from "vue";
type props = {
  id: number;
  name: string;
}[];

export default {
  data() {
    return {
      name: "",
    };
  },
  name: "Add",
  components: {
    Title,
  },
  props: {
    listData: Array as PropType<props | []>,
  },
  methods: {
    addList: function(listData: props, name: string) {
      console.log(listData.length);
      if (listData.length === 0) {
        listData.push({ id: 1, name: name });
      } else {
        const id = Math.max(...listData.map((item) => item.id)) + 1;
        console.log(id);
        listData.push({ id: id, name: name });
      }
    },
  },
};
</script>
