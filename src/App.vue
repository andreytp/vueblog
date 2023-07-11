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
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost() {
      if (this.body.length === 0) {
        return;
      }
      if (this.title.length === 0) {
        return;
      }
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body,
      };
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
    },

  },
}
</script>

<template>
  <div class="app">
    <form @submit.prevent>
      <h4>Post creation</h4>

      <input class="input"
             placeholder="Title"
             type="text"
             v-bind:value="title"
             @input="title=$event.target.value"/>

      <input class="input"
             placeholder="Description"
             type="text"
             v-bind:value="body"
             @input="body=$event.target.value"/>

      <button class="btn"
              @click="createPost">Create
      </button>

    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Title:</strong> {{ post.title }}#{{ post.id }}</div>
      <div><strong>Description:</strong>{{ post.body }} {{ post.id + 1 }}</div>
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