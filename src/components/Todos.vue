<template>
    <div>
        <ul>
            <li v-for="(todo, index) in todos" :key="index">
                <TodoItem :todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
            </li>
        </ul>
    </div>
</template>

<script>
import TodoItem from './TodoItem';

export default {
    name: 'Todos',
    components: {
        TodoItem
    },
    props: [
        'todos'
    ]
}
</script>

<style scoped>

</style>
