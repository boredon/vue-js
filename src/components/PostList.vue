<template>
    <div class="post" v-for="post in posts">
        <div><strong>Title: </strong> {{post.title}}</div>
        <div><strong>Description: </strong> {{post.description}}</div>
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
.post{
    margin-top: 15px;
    border: 1px solid black;
    border-radius: 5px;
    padding: 30px;
    width: 100%;
}
</style>