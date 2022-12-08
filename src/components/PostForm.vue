<template>
    <form @submit.prevent>
        <my-input v-model = "post.title" type="text" placeholder="Title"/>
        <my-input v-model = "post.description" type="text" placeholder="Description"/>
        <my-button @click="createPost"> Add post</my-button>
    </form>
</template>
<script>
import MyButton from './UI/MyButton.vue';
export default {
    components: {
        MyButton
    },
    data(){
        return{
            post: {
                title: '',
                description: '',
            }
        }
    },
    methods: {
        createPost(){
             this.post.id = Date.now();
             this.$emit('create', this.post);
             this.post = {
                title: '',
                description: '',
             }
        }
    }
}
</script>
<style scoped>
form{
    width: 400px;
    display: flex;
    flex-direction: column;
    margin-bottom: 50px;
}

</style>