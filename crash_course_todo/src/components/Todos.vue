<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <div 
            v-for="todo in todos"
            :key="todo.id">
            <TodoItem v-bind:todo="todo"
            v-on:del-todo="$emit('del-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Todos",
    components: {
        TodoItem
    },
    props:["todos"]
    
}
</script>

<style scoped>

</style>