<template>
    <h2 class=" text-center text-4xl text-green-500 pb-5">{{name}}</h2>
</template>

<script lang="ts">
export default {
    name: "Title",
    props:{
        name: String
    }
}
</script>