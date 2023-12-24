<template>
  <article class="blog">
    <h1>Notes</h1>
    <h2 v-if="fetching">Loading...</h2>
    <h2 class="fetch-error" v-if="fetchError">Failed to fetch posts. <div class="retry" v-on:click="fetchPosts">Retry?</div></h2>

    <div class="post" v-for="post in posts" v-bind:key="post.id">
      <h2>{{ post.title }}</h2>
      <div>{{ post.preview }}</div>
      <RouterLink class="read-more" :to="{ name: 'note', params: { slug: post.slug } }">Read more</RouterLink>
    </div>
  </article>
</template>

<script>
import axios from "axios";
export default {
  name: 'BlogView',
  mounted () {
    let self = this
    self.fetchPosts()
  },
  data() {
    return {
      fetching: true,
      fetchError: false,
      posts: [],
    }
  },
  methods: {
    fetchPosts() {
      let self = this
      self.fetchError = false
      self.fetching = true
      axios
        .get('http://localhost:5008/posts')
        .then(response => {
          self.posts = response.data
        })
        .catch(error => {
          console.log(error)
          self.fetchError = true
        })
        .finally(() => this.fetching = false)
    },
  }
}
</script>

<style scoped>
.fetch-error{
  text-align: center;
  color: #C00;
}
.retry{
  color: #1c9c78;
  cursor: pointer;
}
.post{
  border-bottom: 1px solid #DDD;
  padding: 2rem 0rem;
  h2{
    margin-bottom: 0.5rem;
    font-family: 'Abril Fatface', serif;
  }
  .read-more{
    color: #1c9c78;
    margin-top: 5rem;
    font-weight: bold;
  }
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}


</style>
