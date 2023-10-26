<template>
    <div>
        <h1>Greetings, {{username}}</h1>
        <button class="btn logout" @click="logout">Logout</button>
    </div>
    <router-link :to="{name: 'invoices'}">
        <button>Invoices</button>
    </router-link>
</template>

<script>
export default {
    data() {
        return {
            username: window.user
        }
    },
    methods: {
        logout() {
            window.user = null
            this.username = window.user
            this.$router.push({name: 'Home'})
        } 
    }
}
</script>