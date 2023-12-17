<script setup lang="ts">

import { computed } from 'vue'

const emits = defineEmits(['update:inputValue'])
const props = defineProps({
    inputValue:String
}) 

const handerChange = (e:Event)=>{
    const value = (e.target as HTMLInputElement).value;
    emits('update:inputValue',value);
    console.log(value);
}

let value = computed(()=>{
    return props.inputValue;
})

</script>

<template>
    <input :value="value" @input="handerChange" />
</template>

<style scoped>

</style>
