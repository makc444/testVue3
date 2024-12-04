<template>
    <div v-if="posts.length > 0">
        <h3>Список постов</h3>
        <post-item v-for="post in posts" :post="post" :key="post.id" @remove = "$emit('remove', post)"/>
    </div>
    <h2 v-else style="color: firebrick;">Список пользователей пуст</h2>
</template>

<script>
import PostItem from './PostItem.vue'

export default {
    components: { PostItem },
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
    border: 2px solid rgb(24, 165, 59);
    margin-top: 15px;
}

</style>