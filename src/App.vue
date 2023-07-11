<!--https://youtu.be/XzLuMtDelGk?t=1801-->

<script>
export default {
  data() {
    return {
      posts: [
        {id: 0, title: "JavaScript post", body: "Post description"},
        {id: 1, title: "JavaScript post", body: "Post description"},
        {id: 2, title: "JavaScript post", body: "Post description"},
        {id: 3, title: "JavaScript post", body: "Post description"},
      ]

    }
  },
  methods:{
      createPost() {
        
      }
    },

}
</script>

<template>
  <div class="app">
    <form>
      <input class="input" type="text" placeholder="Title">
      <input class="input" type="text" placeholder="Description">
      <button class="btn" @click="createPost">Create</button>

    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Title:</strong> {{post.title}}#{{post.id}}</div>
      <div><strong>Description:</strong>{{post.body}} {{post.id + 1}}</div>
    </div>
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

.post {
  padding: 15px;
  border: 2px solid teal;
  margin-bottom: 15px;
}

form {
  display: flex;
  flex-direction: column;
}

.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

.btn {
  margin-top: 15px;
  margin-bottom: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
  
}

</style>