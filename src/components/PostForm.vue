<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost() {
      // if (this.post.body.length === 0) {
      //   return;
      // }
      // if (this.post.title.length === 0) {
      //   return;
      // }

      this.post.id= Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: '',
        body: '',
      }
    }
  },
}
</script>

<template>
  <form @submit.prevent>

    <h4>Post creation</h4>

    <input class="input"
           placeholder="Title"
           type="text"
           v-model="post.title"/>
<!--           v-bind:value="post.title"-->
<!--           @input="post.title=$event.target.value"-->


    <input class="input"
           placeholder="Description"
           type="text"
           v-model="post.body"
    />
<!--           v-bind:value="post.body"-->
<!--           @input="post.body=$event.target.value"-->


    <button
        class="btn"
        @click="createPost"
    >
      Create
    </button>

  </form>
</template>

<style scoped>
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