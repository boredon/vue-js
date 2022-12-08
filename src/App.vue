<template>
    <div class="main">
        <h1>Posts</h1>
        <post-form @create="createPost"/>
        <post-list :posts="posts"/>
    </div>

</template>
<script>
import PostForm from '@/components/PostForm.vue';
import PostList from '@/components/PostList.vue';
export default {
    components: {
        PostForm,
        PostList
    },
    data(){
        return {
            posts: [
                {id: 1, title: 'Whales', description: 'Description'},
                {id: 2, title: 'Whales 1', description: 'Description 1'},
                {id: 3, title: 'Whales 2', description: 'Description 2'},
            ]
        }
    },
    methods: {
        createPost(post){
            this.posts.push(post)
        },
    }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    
}
.main{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>