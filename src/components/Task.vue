<template>
    <div class="px-6 py-4 rounded-md bg-green-50 shadow mb-4 flex items-center">
        <input type="checkbox" class="w-1/12" v-model="check"/>
        <h3 class="text-lg text-gray-500 w-10/12 line-through" v-if="check">{{name}}</h3>
        <h3 class="text-lg text-gray-500 w-10/12 " v-else>{{name}}</h3>
       
    </div>
</template>

<script lang="ts">
export default{
    data(){
        return {
            check:false
        }
    },
    name: "Task",
    props:{
        id: Number,
        name:String
    }
}
</script>