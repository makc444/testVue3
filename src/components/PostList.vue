<template>
    <div>
        <h3>Список пользователей</h3>
        <div class="post" v-for="post in posts" :key="post.id"> <strong> Название: </strong> {{post.title}} <div><strong> Описание: </strong> {{post.body}} </div> </div>
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
    border: 2px solid rgb(24, 165, 59);
    margin-top: 15px;
}

</style>