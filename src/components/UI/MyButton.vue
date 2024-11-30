<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'my-button'
}

</script>

<style scoped>

.btn {
    border: 3px solid rgb(8, 199, 199);
    padding: 10px 20px;
    margin-top: 15px;
    background: none;
    color: rgb(16, 12, 231);
    /*background-color: rgb(69, 42, 165);*/
}

</style>