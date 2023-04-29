<template>
<div>
  <h1 class="text-3xl font-bold underline"> {{ name ? name : "Hello PowerHumans" }}</h1>
  <h2>{{ post.data.title }}</h2>
</div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'IndexPage',
  async asyncData({ params }) {
      const post = await axios.get(`https://api.nuxtjs.dev/posts/1`)
      return { post }
    }
}
</script>
