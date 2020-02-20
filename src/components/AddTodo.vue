<template>
    <div>
        <form @submit="addTodo" >
            <input type="text" v-model="title" name="title" placeholder="Add Todo...">
            <input type="submit" value="Submit" class="btn">
        </form>
    </div>
</template>

<script>
    // const uuidv4 = require('uuid/v4');
    
    export default {
        name: "AddTodo",
        data() {
            return {
                title: ''
            }
        },
        methods: {
            addTodo(e) {
                e.preventDefault();
                // We don't want to event to actually try to submit to a file
                // Stop default behavior, create todo, and emit the event
                const newTodo = {
                    title: this.title,
                    completed: false
                }

                this.$emit('add-todo', newTodo)

                this.title = '';
            }
        }
    }
</script>

<style scoped>
    form {
        display: flex; 
    }

    input[type="text"] {
        flex: 10;
        padding: 5px;
    }

    input[type="submit"] {
        flex: 2;
    }
</style>