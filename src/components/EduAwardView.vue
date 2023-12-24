<template>
  <div class="education">

    <div class="row">
      <div class="institution">{{ institution }}</div>
      <div class="year">{{ year }}</div>
    </div>


    <div class="image">
      <img :src="'/'+image" :alt="institution"/>
    </div>

    <div class="title">{{ title }}</div>

    <div class="description">
      {{ description }}
    </div>
  </div>
</template>
<script>
export default {
  name: 'EduAwareView',
  props: {
    title: String,
    year: String,
    institution: String,
    image: String,
    description: String,
  }
}
</script>
<style>
.education {
  border-radius: 0.75rem;
  border: 1px solid #ccc;
  background-color: #FFF;
  padding: 1.5rem;
  text-align: center;
  margin-bottom: 1.5rem;
  max-width: 640px;
  margin-left: auto;
  margin-right: auto;
  .row{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-weight: 700;
    color: #555;
  }
    .title{
      color: #1c9c78;
      margin-bottom: 0.5rem;
      font-size: 1.15rem;
    }
  .image{
    text-align: center;
    padding: 2.5rem 0.25rem;
    img{
      max-width: 50%;
    }
  }
  .institution{
    font-weight: 700;
    font-size: 1.2rem;
    margin-bottom: 0.75rem;
  }
  .description{
    font-size: 0.85rem;
    color: #333;
  }
}

</style>