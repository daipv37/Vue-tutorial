<template>
    <footer><h2>{{ title }}</h2></footer>    
</template>

<script>
export default {
    name: 'comp-footer',
    props: {
        title: {
            type: String,
            default: null
        }
    },
    data() {
        return {
            text: 'Footer'
        }
    }
}
</script>

<style>

</style>