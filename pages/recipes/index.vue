<template>
  <section class="recipes">
		<Recipe 
		  v-for="recipe in recipes" 
		  :key="recipe.id"
		  :thumbnail="recipe.thumbnail"
			:title="recipe.title"
			:previewText="recipe.previewText"
			:id="recipe.id"
		/>
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";
export default {
	data () {
		return {

		}
	},

	components: {
		Recipe
	},

	/**
	 * @description data from server
	 */ 
	asyncData () {
    return new Promise((resolve, reject) => {
			setTimeout(() => {
				resolve({
					recipes: [
						{
							id: '1',
							title: 'Delicious Pizza',
							previewText: 'Awesome Pizza',
							thumbnail: 'https://static.pexels.com/photos/326278/pexels-photo-326278.jpeg'
						},
						{
							id: '2',
							title: 'Delicious vigetable',
							previewText: 'Awesome vigetable',
							thumbnail: 'https://images.pexels.com/photos/5938/food-salad-healthy-lunch.jpg'
						}
					]
				});
			}, 1500)
		})
	},

}
</script>

<style scoped>
.recipes
{
  display: flex;
	flex-flow: row wrap;
	justify-content: center;
	align-items: center; 
}
</style>
