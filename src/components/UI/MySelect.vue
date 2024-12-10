<template>
    <select v-model="modeleValue" @change="changeOption">
        <option disabled value="">Выберите из списка</option>
        <option v-for="option in options" :key="option.value" :value="option.value">{{ option.name }}</option>
    </select>
</template>

<script>
    export default {
        name: 'my-select',
        props: {
            modelValue: {
                type: String
            },
            options: {
                type: Array,
                default: () => []
            }
        },
        methods: {
            changeOption(option){
                this.$emit('update:modelValue', options)            }
        }
    }
</script>

<style scoped>

</style>