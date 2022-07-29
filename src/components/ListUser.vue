<template>
    <div class="listUser">
        <user
            v-for="user in listUsers"
            v-bind:key="user.id"
            v-bind:user="user"
            v-on:deleteUser="deleteUser"
        />
    </div>
</template>

<script>
import User from './User.vue'
export default {
  components: { User },
    name: 'list-user',
    props: {
        listUsers: {
                type: Array,
                default: []
            }
    },
    data() {
        return {
            
        }
    },
    methods: {
        deleteUser(data) {
            this.$emit("handleDeleteUser", data);
        }
    }
}
</script>

<style>
    .listUser {
        justify-content: center;
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }
</style>