<script setup>
import { useTodoListStore } from "@/stores/todoList";
import { storeToRefs } from "pinia";

const store = useTodoListStore();

// storeToRefs lets todoList keep reactivity:
const { todoList } = storeToRefs(store);
</script>

<template>
  <div v-for="todo in todolist" :key="todo.id">
    <div class="content">
      <span>{{ todo.item }}</span>
    </div>
  </div>
</template>

<style scoped></style>
