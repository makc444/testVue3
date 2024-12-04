<template>
    <div class="app">
        <post-form @create="createPost"/>
        <post-list :posts="posts" @remove="removePost"/>
    </div>
</template>

<script>
import PostForm from './components/PostForm.vue'
import PostList from '@/components/PostList.vue'

  export default {
    components: {
        PostList, PostForm 
    },
      data() {
        return {
          posts: [
            {id: 1, title: 'JavaScript', body: 'Описание поста'},
            {id: 2, title: 'JavaScript 2', body: 'Описание поста 2'},
            {id: 3, title: 'JavaScript 3', body: 'Описание поста 3'},
            {id: 4, title: 'JavaScript 4', body: 'Описание поста 4'},
            {id: 5, title: 'JavaScript 5', body: 'Описание поста 5'},
            {id: 6, title: 'JavaScript 6', body: 'Описание поста 6'}
          ],    
        }
      },
      methods: {
          createPost(post) {
                this.posts.push(post);      
            },
          removePost(post) {
              this.posts = this.posts.filter(p => p.id !== post.id)
          } 
        },
  }
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 20px;
}
</style>