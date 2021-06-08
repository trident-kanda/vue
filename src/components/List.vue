<template>
  <div class="p-5">
    <Title name="LIST" />
    <Task
      v-for="item in listData"
      :name="item.name"
      :id="item.id"
      :listData="listData"
      :key="item.id"
      :deleteList="deleteList"
    />
  </div>
</template>

<script lang="ts">
import Title from "./Title.vue";
import Task from "./Task.vue";
import { PropType } from "vue";
type props = {
  id: number;
  name: string;
}[];

export default {
  name: "Vue",
  components: {
    Title,
    Task,
  },
  props: {
    listData: Array as PropType<props | []>,
    deleteList: Function,
  },
};
</script>
