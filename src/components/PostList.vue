<template>
  <div>
    <h3>Post list</h3>
    <PostItem
        v-for="post in posts"
        :post="post"
    />

  </div>
</template>

<script>
import PostItem from "@/components/PostItem.vue";

export default {
  components: {PostItem},
  props: {
    posts: {
      type: Array,
      required: true

    }
  }
}
</script>

<style scoped>


</style>