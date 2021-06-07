<template>
  <input
    value=""
   />
</template>

<script>
export default {
    name: 'Input',
    props: {}
}
</script>

<style scoped>
    input {
        display: flex;
        justify-content: center; 
        align-items: center;
        margin-bottom: 20px;
        height: 30px;
        border: 1px solid steelblue;
        border-radius: 5px;
        font-size: large;
        padding: 1rem;
    }
    input:focus {
        outline: none;
    }
</style>