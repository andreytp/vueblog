<!--https://youtu.be/XzLuMtDelGk?t=1801-->

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {PostList, PostForm},
  data() {
    return {
      posts: [
        {id: 0, title: "JavaScript post", body: "Post description"},
        {id: 1, title: "JavaScript post", body: "Post description"},
        {id: 2, title: "JavaScript post", body: "Post description"},
        {id: 3, title: "JavaScript post", body: "Post description"},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
}
</script>

<template>
  <div
      class="app"
  >
    <PostForm @create="createPost"/>
    <PostList :posts="posts"/>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}




</style>