<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 0,
    }
  },
  methods:{
    addlike() {
      this.likes += 1;
    },
    adddislike() {
      this.dislikes += 1;
    },
  },
}
</script>

<template>
  <div>
    <div>
      <button @click="addlike">Like</button>
      <button @click="adddislike">Dislike</button>
    </div>
    <div>Likes {{ likes }}</div>
    <div>DisLikes {{ dislikes }} </div>
  </div>

</template>

<style scoped>

</style>