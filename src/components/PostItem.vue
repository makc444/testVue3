<template>  
        <div class="post">
            <div><strong>Название поста: </strong>{{post.title}}</div>
            <div><strong>Описание поста: </strong>{{post.body}}</div>
        </div>  
        <div class="post__btns">
            <my-button>Удалить</my-button>    
        </div>     
</template>

<script>
export default {
    props: {
        post: {
            type: Object,
            required: true
        }
    },
}

</script>

<style scoped>  
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
    display: flex;
    align-items: center;
    justify-self: space-between;
}
</style>