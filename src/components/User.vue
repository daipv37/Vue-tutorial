<template>
    <div class="user">
        <p v-if="user.isActice == true">{{ user.email }}</p>
        <button
            v-on:click="handleDelete" 
            class="delete">Delete</button>
    </div>
</template>

<script>
export default {
    name: 'user',
    props: {
        user: {
            type: Object,
            default: null
        }
    },
    data() {
        return {
            text: 'User'
        }
    },
    methods: {
        handleDelete(e) {
            var data = {
                id: this.user.id
            }

            this.$emit("deleteUser", data);
        }
    }
}
</script>

<style>
    .user {
        width: 20%;
        border: 1px solid gray;
    }
    .user .delete {
        top: 0;
        right: 0;
    }
</style>