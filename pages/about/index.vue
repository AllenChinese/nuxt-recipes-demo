/**
 * @Description: about
 */
<template>
<div>
  <h1>THE ABOUT PAGE</h1>
   <div class="recipe-image">
      <img :src="recipe.thumbnail" :alt="recipe.previewText">
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      recipe: {
        previewText: 'Awesome Pizza',
				thumbnail: require('@/assets/images/food1.jpg')
      }
    }
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
}
.recipe-image {
  margin: 0 auto;
  text-align: center;
}
</style>

