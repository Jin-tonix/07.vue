<script setup>
import{ref}from 'vue';
import DynamicChild from './DynamicChild.vue';

const dynamicName = ref("name");
</script>

<template>
<div>
    <h1>DynamicSlot : </h1>
    <input v-model = "dynamicName"/>
    <DynamicChild>
        <template #[dynamicName]>
            {{ dynamicName }}
            <img src ="https://campaign.vake.io/wp-content/uploads/2021/01/a%E1%84%92%E1%85%A9%E1%86%BC%E1%84%80%E1%85%B5%E1%86%AF%E1%84%83%E1%85%A9%E1%86%BC.png">;
        </template>
    </DynamicChild>
</div>
</template>

<style scoped>
.parentsContainer{
    display : flex;
    align-items: center;
    flex-direction: colum;
    border: 1px solid;
}

img{
    width: 80px
}

</style>