<template>
  <button @click="onClick" class="btn">{{name}}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        name: String,
    },
    methods: {
        onClick() {
            this.$emit('klikaj')
        }
    }

}
</script>

<style>

</style>