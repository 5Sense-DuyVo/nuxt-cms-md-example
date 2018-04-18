<template>
  <div>
    <div>記事id: {{ blog.id }}</div>
    <div>
      <div>記事tags</div>
      <div v-for="tag in blog.tags">　{{ tag }}</div>
    </div>
    <div v-html="blog.html"></div>
    <nuxt-link :to="{ path: `/` }">Back List</nuxt-link>
  </div>
</template>

<script>
export default {
  asyncData({ params }) {
    return {
      blog: require(`~/static/models/blogs/${params.id}.json`),
    }
  },
}
</script>
