<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <!-- picture -->
      <div class="thumbnail" :style="{ backgroundImage: 'url('+ thumbnail +')' }"></div>
      <!-- title -->
      <h1>{{ title }}</h1>
      <!-- decription -->
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  data () {
    return {
      
    }
  },

  props: [ 'thumbnail', 'title', 'previewText', 'id' ]
}
</script>

<style scoped>
a
{
  text-decoration: none;
}
.recipe
{
  width: 280px;
  padding: 8px;
  margin: 10px;
  border: 1px solid #ccc;
  box-sizing: border-box;
  box-shadow: 0 2px 2px #aaa;
}

.thumbnail 
{
	width: 100%;
	height: 200px;
  background-position: center;
	background-size: cover;
}
</style>
