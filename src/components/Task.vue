<template>
    <div class="px-6 py-4 rounded-md bg-green-50 shadow mb-4 flex items-center">
        <input type="checkbox" class="w-1/12" />
        <h3 class="text-lg text-gray-500 w-10/12 ">{{name}}</h3>
    </div>
</template>

<script lang="ts">

export default{
    name: "Task",
    props:{
        id: Number,
        name:String
    }
}
</script>