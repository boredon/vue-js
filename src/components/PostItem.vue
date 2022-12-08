<template>
    <div class="post">
        <div><strong>Title: </strong> {{post.title}}</div>
        <div><strong>Description: </strong> {{post.description}}</div>
        <div class="post_btns">
            <my-button @click="removePost" class="delete">Remove</my-button>
        </div>
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
    data(){
        return {
            removePost(){

            }
        }
    }
}
</script>
<style scoped>
.post{
    margin-top: 15px;
    border: 1px solid black;
    border-radius: 5px;
    padding: 30px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.delete{
    margin-top: 50px;
    padding: 10px 15px;
}
</style>