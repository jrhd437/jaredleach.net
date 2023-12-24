<template>
  <article class="blog">
    
    <h2 v-if="fetching">Loading...</h2>
    <h2 class="fetch-error" v-if="fetchError">Failed to fetch note.</h2>
    <article class="post" v-if="!fetching && !fetchError">
        <h1>{{ post.title }}</h1>
      <div v-html="post.article"></div>
    </article>
  </article>
</template>

<script>
//http://localhost:5008/posts/{slug}
import axios from "axios";
export default {
  name: 'NoteView',
  mounted () {
    let self = this
    self.fetchPost()
  },
  params: {
    slug: String
  },
  data() {
    return {
      fetching: true,
      fetchError: false,
      post: [],
    }
  },
  methods: {
    fetchPost() {
      let self = this
      self.fetchError = false
      self.fetching = true
      axios
        .get('http://localhost:5008/posts/'+this.$route.params.slug)
        .then(response => {
          self.post = response.data[0]
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
h2{
  font-family: 'Abril Fatface', serif;
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}


</style>
