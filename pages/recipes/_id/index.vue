/**
 * @Description: recipe
 */
<template>
  <section class="single-recipe">
    <h1 class="recipe-title">{{ recipe.title }}</h1>
    <div class="recipe-image">
      <img :src="recipe.thumbnail" :alt="recipe.previewText">
    </div>
    <p class="recipe-content">{{ recipe.descriptionText }}</p>
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
              descriptionText: '随着日币的贬值，无论是从facebook、instagram或是新闻上，每天都能看到有关日本的讯息。当然，来到日本最不能错过的就是美食了。对于初次来到日本的你，也许在机票、住宿的钱都能清楚并规划好自己的预算。但是对于饮食这部分的费用，要怎么拿捏，是不是觉得有点不好掌握呢？这次LIVE JAPAN要跟大家介绍，来日本玩，分别从早、中、晚餐，加上下午茶的消费，这样一来就可以掌握好自己的预算了。',
							thumbnail: require('@/assets/images/food1.jpg')
						},
						{
							id: '2',
							title: 'Delicious vigetable',
              previewText: 'Awesome vigetable',
              descriptionText: '东京有很多好吃的日本料理店，不过偶尔也想换一下口味……是的，有时会特别想吃汁多味美的汉堡。但是，即使是美食街的东京，想要品尝真正的汉堡也须要在寻找上下点工夫。此次就是献给汉堡控的专题文章，为您介绍的当然都是提供汉堡配上薯条的完美汉堡店！从最近流行的加州风味到日式汉堡，乃至非常适合马天尼酒的纽约风味汉堡店，只要您看过下述的汉堡店列表，一定能找到符合您口味的店。就让我们为您介绍以味道、人气度、氛围为基准严选出的汉堡店！',
							thumbnail: require('@/assets/images/food2.jpg')
						},
						{
							id: '3',
							title: 'Delicious sweet corn',
              previewText: 'Awesome sweet corn',
              descriptionText: '在隅田川北岸筑地一带，有日本代表性的大型水产批发市场“筑地市场”，市场内既有专供超市、鲜鱼店、寿司店的食材市场，也有供普通市民购买和餐饮的“鱼横丁”区域。市场的招牌——金枪鱼拍卖活动一向极具人气，连外国游客也争相大饱眼福。但该活动不接受提前预约，从开场当天的早晨五点开始入场手续，但由于报名者众多，所以只允许前120人入场。有可能还没到原定的入场时间就报名截止了，所以想一睹为快的话一定要早早报名哦！筑地市场有可能搬迁到丰洲，所以要把握最后的筑地市场就要趁现在了。筑地市场周边还聚集了大量餐饮店和小型市场，使这一地区更加充满活力和人气。另外，要去筑地市场的话在早上9点到下午2点之间最推荐，需特别注意很多店都会在星期日休息，去之前请到官网查询相关信息。这次我们在鱼市场氛围浓郁的“鱼横丁”和周边地区精心挑选了四家有特色的寿司名店，请您一定不要错过哦！',
							thumbnail: require('@/assets/images/food3.jpg')
						},
						{
							id: '4',
							title: 'Delicious beef',
              previewText: 'Awesome beef',
              descriptionText: '被刊登于世界著名美食指南的老铺，在此可享用关东式寿喜烧套餐（9720日元起）。全部座位为完全独立的榻榻米包间，非常适合喜欢宽敞舒适地用餐的人。充满传统性的茶室式的和室，让人感受到美好的昔日日本。',
							thumbnail: require('@/assets/images/food1.jpg')
						},
						{
							id: '5',
							title: 'Delicious pork',
              previewText: 'Awesome pork',
              descriptionText: '成吉思汗蒙古烤肉是北海道的名产，是在中间凸起的烤盘上烤羊肉的一道料理。大多数店家使用的都是澳洲、新西兰及冰岛产的羊肉，但也有少数店家会使用北海道产的羊肉与虾夷鹿肉。成吉思汗烤肉有两种吃法，一种是将肉烤好后沾上酱汁吃，一种是先将肉用酱汁腌入味，再烤来吃，不同店都各有特色，互相比较也是一种乐趣！',
							thumbnail: require('@/assets/images/food2.jpg')
						},
						{
							id: '6',
							title: 'Delicious pea',
              previewText: 'Awesome pea',
              descriptionText: '若是想要毫无忌惮地大品甜点的话，就一定要去有甜点吃到饱的店家！在东京甜点吃到饱的店家非常多，使用大量当季水果制成的甜点做主打、独特的点餐式甜点吃到饱等等，每家店的主打风格都不太一样。这次严选5间位于东京市区的甜点吃到饱店家推荐给各位！',
							thumbnail: require('@/assets/images/food3.jpg')
						}
					].find(el => el.id === context.params.id)
				});
			}, 1500)
    })

  }

}
</script>

<style>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: 990px;
  text-align: center;
  padding: 30px;
}
.recipe-title {
  margin-bottom: 20px;
  font-size: 36px;
}

.recipe-image img {
  width: 500px;
}

.recipe-content {
  padding: 20px 0;
  width: 500px;
  line-height: 22px;
  text-align: left;
}
</style>

