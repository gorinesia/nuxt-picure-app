<template>
  <section class="recipes">
    <Recipe 
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.previewText" /> 
  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },
  data() {
    return {
      recipes: [
        {
          id: "1",
          title: '盛り合わせ(中)',
          previewText: "¥ 1,200円",
          thumbnail: 'http://www.atpress.ne.jp/releases/52102/img_52102_1.jpg'
        },
        {
          id: "2",
          title: '盛り合わせ(大)',
          previewText: "¥ 2,000円",
          thumbnail: 'https://i.ytimg.com/vi/UGJ11p6MHNI/maxresdefault.jpg'
        },
        {
          id: "3",
          title: '梅',
          previewText: "¥ 3,500円",
          thumbnail: 'https://blog-001.west.edge.storage-yahoo.jp/res/blog-92-53/kazuon0728/folder/1868438/64/69687564/img_0'
        },
        {
          id: "4",
          title: '竹',
          previewText: "¥ 5,000円",
          thumbnail: 'http://blogs.c.yimg.jp/res/blog-9e-a0/mikuniotouto/folder/1188704/62/39948562/img_0'
        },
        {
          id: "5",
          title: '松',
          previewText: "¥ 7,000円",
          thumbnail: 'https://up.gc-img.net/post_img_web/2017/07/ox8nm8Boyre9fFC_22646.png'
        },
        {
          id: "6",
          title: '特上盛り合わせ',
          previewText: "¥ 10,000円",
          thumbnail: 'http://image.space.rakuten.co.jp/d/strg/ctrl/9/6f99f0a3d2e65a9037951234408c26ef04d9fc2d.93.2.9.2.jpeg'
        },
      ]
    }
  }
  // asyncData() {
  //   return new Promise((resolve, reject) => {
  //     setTimeout(() => {
  //       resolve({
  //         recipes: [
  //           {
  //             id: "1",
  //             title: '盛り合わせ(中)',
  //             previewText: "¥ 1,200円",
  //             thumbnail: 'http://www.atpress.ne.jp/releases/52102/img_52102_1.jpg'
  //           },
  //           {
  //             id: "2",
  //             title: '盛り合わせ(大)',
  //             previewText: "¥ 2,000円",
  //             thumbnail: 'https://i.ytimg.com/vi/UGJ11p6MHNI/maxresdefault.jpg'
  //           },
  //           {
  //             id: "3",
  //             title: '梅',
  //             previewText: "¥ 3,500円",
  //             thumbnail: 'https://blog-001.west.edge.storage-yahoo.jp/res/blog-92-53/kazuon0728/folder/1868438/64/69687564/img_0'
  //           },
  //           {
  //             id: "4",
  //             title: '竹',
  //             previewText: "¥ 5,000円",
  //             thumbnail: 'http://blogs.c.yimg.jp/res/blog-9e-a0/mikuniotouto/folder/1188704/62/39948562/img_0'
  //           },
  //           {
  //             id: "5",
  //             title: '松',
  //             previewText: "¥ 7,000円",
  //             thumbnail: 'https://up.gc-img.net/post_img_web/2017/07/ox8nm8Boyre9fFC_22646.png'
  //           },
  //           {
  //             id: "6",
  //             title: '特上盛り合わせ',
  //             previewText: "¥ 10,000円",
  //             thumbnail: 'http://image.space.rakuten.co.jp/d/strg/ctrl/9/6f99f0a3d2e65a9037951234408c26ef04d9fc2d.93.2.9.2.jpeg'
  //           },
  //         ]
  //       })
  //     }, 1500)
  //   })
  // }
}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}

.recipe {
  box-align: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>