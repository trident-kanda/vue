<template>
    <div class="p-5">
        <Title name="LIST"/>
        <Task id=123 name="aaa"/>
    </div>
</template>

<script lang="ts">

import Title from "./Title.vue"
import Task from "./Task.vue"

export default{
    name:"Vue",
    components:{
        Title,
        Task
    }
}
</script>