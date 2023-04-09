<template>
  <ul>
    <li>Home</li>
    <li>About Us</li>
    <li>Contact Us</li>
  </ul>
  <h1 v-if="title">Title</h1>
  <h1>Posts</h1>
  <div class="list">
    <div v-for="post in posts" :key="post.title">
      <h3>{{ post.title }}</h3>
      <h4>{{ post.description }}</h4>
      <p>{{ post.content }}</p>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
const title = true
const posts = reactive([
  { title: 'Guillem', description: 'The oldest brother', content: 'I make the rules' },
  { title: 'Gerard', description: 'The middle brother', content: 'Rules make for me' },
  { title: 'Carlota', description: 'The youngest sister', content: 'Rules don`t apply to me' }
])
</script>

<style scoped>
ul {
  display: flex;
  list-style: none;
  gap: 1em;
}
.list {
  display: flex;
  gap: 30px;
}
h3 {
  background-color: grey;
}
</style>