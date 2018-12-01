/**
 * @Description: recipes
 */
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
							thumbnail: require('@/assets/images/food1.jpg')
						},
						{
							id: '2',
							title: 'Delicious vigetable',
							previewText: 'Awesome vigetable',
							thumbnail: require('@/assets/images/food2.jpg')
						},
						{
							id: '3',
							title: 'Delicious sweet corn',
							previewText: 'Awesome sweet corn',
							thumbnail: require('@/assets/images/food3.jpg')
						},
						{
							id: '4',
							title: 'Delicious beef',
							previewText: 'Awesome beef',
							thumbnail: require('@/assets/images/food1.jpg')
						},
						{
							id: '5',
							title: 'Delicious pork',
							previewText: 'Awesome pork',
							thumbnail: require('@/assets/images/food2.jpg')
						},
						{
							id: '6',
							title: 'Delicious pea',
							previewText: 'Awesome pea',
							thumbnail: require('@/assets/images/food3.jpg')
						}
					]
				});
			}, 1500)
		})
	},

}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
  margin: 50px auto;
  width: 990px;
}
</style>
