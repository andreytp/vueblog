<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}

</script>

<template>
  <div class="post" >
    <div><strong>Title:</strong> {{ post.title }}#{{ post.id }}</div>
    <div><strong>Description:</strong>{{ post.body }} {{ post.id + 1 }}</div>
  </div>
</template>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-bottom: 15px;
}

</style>