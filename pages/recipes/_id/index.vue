<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div class="recipe-image">
      <img :src="recipe.thumbnail" :alt="recipe.previewText">
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  /**
	 * @description data from server
	 */ 
	asyncData (context) {

    return new Promise((resolve, reject) => {
			setTimeout(() => {
				resolve({
					recipe: [
						{
							id: '1',
							title: 'Delicious Pizza',
              previewText: 'Awesome Pizza',
              descriptionText: 'This is a nice Pizza',
							thumbnail: 'https://static.pexels.com/photos/326278/pexels-photo-326278.jpeg'
						},
						{
							id: '2',
							title: 'Delicious vigetable',
              previewText: 'Awesome vigetable',
              descriptionText: 'This is a awesome vigetable',
							thumbnail: 'https://images.pexels.com/photos/5938/food-salad-healthy-lunch.jpg'
						}
					].find(el => el.id === context.params.id)
				});
			}, 1500)
    })
    
  }
  
}
</script>

<style>
.single-recipe
{
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
.recipe-image img
{
  width: 80%;
}
</style>

