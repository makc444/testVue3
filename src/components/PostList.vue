<template>
    <div>
        <h3>Список пользователей</h3>
        <post-item v-for="post in posts" :post="post"/>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>      

.post {
    padding: 15px;
    border: 2px solid rgb(0, 0, 0);
    margin-top: 15px;
}

</style>