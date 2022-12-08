<template>
    <button>
        <slot></slot>
    </button>
</template>
<script>
export default {
    name: 'my-button'
}
</script>
<style scoped>
button{
    border: 1px solid white;
    font-family: Georgia, 'Times New Roman', Times, serif;
    border-radius: 10px;
    margin-top: 15px;
    padding: 10px 15px;
}
</style>