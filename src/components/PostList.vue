<template>
    <div>
        <h1>List of users</h1>
        <post-item v-for="post in posts" :post="post"/>
    </div>
</template>

<script>
import PostItem from './PostItem.vue';
export default {
    components: {
        PostItem
    },
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>
<style scoped>
div{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
</style>