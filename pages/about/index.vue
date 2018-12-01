/**
 * @Description: about
 */
<template>
<div>
  <h1>THE ABOUT PAGE</h1>
  <div class="link-part">
    <p v-for="item in linkData">
      <a :href="item.url">
        {{item.name}}
      </a>
    </p>
  </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      linkData: [
        {
          url: 'https://zh.nuxtjs.org/',
          name: 'NUXT'
        },
        {
          url: 'https://github.com/AllenChinese',
          name: 'MY Github'
        },
        {
          url: 'https://www.pexels.com',
          name: 'Nice Pexels'
        }
      ]
    }
  }
}
</script>

<style scoped>
h1 {
  margin: 20px;
  text-align: center;
}
.link-part {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  width: 500px;
}
</style>

