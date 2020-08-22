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
          title: '激辛ラーメン',
          previewText: "¥ 850円",
          thumbnail: 'https://www.ibarakindp.com/wp-content/uploads/2017/06/P6232015.jpg'
        },
        {
          id: "2",
          title: '超激辛ラーメン',
          previewText: "¥ 900円",
          thumbnail: 'http://www.karairamen14.com/images/material/sp_image1.jpg'
        },
        {
          id: "3",
          title: '地獄ラーメン',
          previewText: "¥ 950円",
          thumbnail: 'https://stat.ameba.jp/user_images/20180221/23/gekikaramikan/04/f9/j/o0480045314136215760.jpg'
        },
        {
          id: "4",
          title: '旨辛ラーメン',
          previewText: "¥ 950円",
          thumbnail: 'http://cdn-ak.f.st-hatena.com/images/fotolife/g/g-gourmedia/20140629/20140629142630.jpg'
        },
        {
          id: "5",
          title: '四川風麻婆豆腐',
          previewText: "¥ 900円",
          thumbnail: 'http://www.initialsite.com/wp-content/uploads/2014/12/IMG_3262.jpg'
        },
        {
          id: "6",
          title: '激辛麻婆豆腐',
          previewText: "¥ 950円",
          thumbnail: 'https://tblg.k-img.com/resize/1200x630c/restaurant/images/matome/2264/262e4af4ceb51ff690b8055ed73c4d28.jpg?token=3745007&api=v2'
        }
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
  //             title: '激辛ラーメン',
  //             previewText: "¥ 850円",
  //             thumbnail: 'https://www.ibarakindp.com/wp-content/uploads/2017/06/P6232015.jpg'
  //           },
  //           {
  //             id: "2",
  //             title: '超激辛ラーメン',
  //             previewText: "¥ 900円",
  //             thumbnail: 'http://www.karairamen14.com/images/material/sp_image1.jpg'
  //           },
  //           {
  //             id: "3",
  //             title: '地獄ラーメン',
  //             previewText: "¥ 950円",
  //             thumbnail: 'https://stat.ameba.jp/user_images/20180221/23/gekikaramikan/04/f9/j/o0480045314136215760.jpg'
  //           },
  //           {
  //             id: "4",
  //             title: '旨辛ラーメン',
  //             previewText: "¥ 950円",
  //             thumbnail: 'http://cdn-ak.f.st-hatena.com/images/fotolife/g/g-gourmedia/20140629/20140629142630.jpg'
  //           },
  //           {
  //             id: "5",
  //             title: '四川風麻婆豆腐',
  //             previewText: "¥ 900円",
  //             thumbnail: 'http://www.initialsite.com/wp-content/uploads/2014/12/IMG_3262.jpg'
  //           },
  //           {
  //             id: "6",
  //             title: '激辛麻婆豆腐',
  //             previewText: "¥ 950円",
  //             thumbnail: 'https://tblg.k-img.com/resize/1200x630c/restaurant/images/matome/2264/262e4af4ceb51ff690b8055ed73c4d28.jpg?token=3745007&api=v2'
  //           },
  //         ]
  //       })
  //     }, 1500)
  //   })
  // }
}
</script>

<style scoped>
h1 {
  text-align: center;
}

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