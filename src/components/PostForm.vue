<template>
    <form @submit.prevent>
        <input v-model = "post.title" class="input" type="text" placeholder="Title">
        <input v-model = "post.description" class="input" type="text" placeholder="Description">
        <button @click="createPost">Add post</button>
    </form>
</template>
<script>
export default {
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
.input, button{
    margin-top: 15px;
}
button{
    padding: 10px 15px;
}
</style>