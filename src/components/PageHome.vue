<template>
  <div>Hello from Home Page</div>
  <div v-for="thread in threads" :key="thread.id">
    <h2>
      {{ thread.title }}
    </h2>
    <div v-for="postId in thread.posts" :key="postId">
      <h4>{{ userById(postById(postId).userId).name }}</h4>
      <p>{{ postById(postId).text }}</p>
    </div>
  </div>
</template>

<script>
import dummyData from "@/data.json";
export default {
  data() {
    return {
      threads: dummyData.threads,
      users: dummyData.users,
      posts: dummyData.posts,
    };
  },
  methods: {
    postById(postId) {
      return this.posts.find((p) => p.id === postId);
    },
    userById(userId) {
      return this.users.find((u) => u.id === userId);
    },
  },
};
</script>

<style>
</style>