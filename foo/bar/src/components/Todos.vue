<template>
    <div :key="todo.id" v-for="todo in todos">
        <h3>{{task.text}}</h3>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'
export default {
    name: 'Todos',
    props: {
        todos: Array
    }
}
</script>
