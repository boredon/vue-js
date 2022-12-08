<template>
    <input :value="modelValue" class="input" @input="editPost">
</template>
<script>
export default {
    name: 'my-input',
    props:{
        modelValue: [String, Number]
    },
    methods: {
        editPost(e){
            this.$emit('update:modelValue', e.target.value)
        }
    }
}
</script>
<style scoped>
.input{
    padding: 10px 20px;
    margin-top: 15px;
}
</style>