<template>
    <header class="header">
        <h1>Todo List</h1>
        <div id="nav">
            <router-link to="/">Todo List</router-link> |
            <router-link to="/about">About</router-link>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>

    .header {
        background: #333;
        color: white;
        text-align: center;
        padding: 10px;
    }

    .header a {
        color: white;
        padding-right: 5px;
        text-decoration: none;
    }
    
</style>