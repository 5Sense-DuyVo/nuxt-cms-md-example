<template>
  <div>
    <ul>
      <li v-for="blog in blogs">
        <nuxt-link :to="{ path: `/blogs/${blog.id}/` }">Read {{ blog.id }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  asyncData() {
    return {
      blogs: require('~/static/models/blogs/list.json')
    }
  },
}
</script>
