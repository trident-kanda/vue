<template>
  <div class="px-6 py-4 rounded-md bg-green-50 shadow mb-4 flex items-center">
    <input type="checkbox" class="w-1/12" v-model="check" />
    <h3 class="text-lg text-gray-500 w-10/12 line-through" v-if="check">
      {{ name }}
    </h3>
    <h3 class="text-lg text-gray-500 w-10/12 " v-else>{{ name }}</h3>
    <TrashIcon :listData="listData" :id="id" :deleteList="deleteList" />
  </div>
</template>

<script lang="ts">
import TrashIcon from "./TrashIcon.vue";
import { PropType } from "vue";
type state = {
  check: boolean;
};
type props = {
  id: number;
  name: string;
}[];
export default {
  data(): state {
    return {
      check: false,
    };
  },
  components: {
    TrashIcon,
  },
  name: "Task",
  props: {
    id: Number,
    name: String,
    listData: Array as PropType<props | []>,
    deleteList: Function,
  },
};
</script>
