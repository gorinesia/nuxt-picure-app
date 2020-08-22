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
          title: 'カバ蔵',
          previewText: "むしゃむしゃ",
          thumbnail: 'http://www.tobuzoo.com/zoo/list/details/pc/0_an_21_03.jpg'
        },
        {
          id: "2",
          title: 'カバ吉',
          previewText: "ぐおーー",
          thumbnail: 'https://cdn-ak.f.st-hatena.com/images/fotolife/N/NishImO/20110202/20110202004023.jpg'
        },
        {
          id: "3",
          title: 'カバごろう',
          previewText: "ぼてっ",
          thumbnail: 'https://i.ytimg.com/vi/jYx4qY9ze5o/maxresdefault.jpg'
        },
        {
          id: "4",
          title: 'カバ山さん',
          previewText: "むーーん",
          thumbnail: 'https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Mother_and_very_small_baby_hippo.jpg/200px-Mother_and_very_small_baby_hippo.jpg'
        },
        {
          id: "5",
          title: 'カバざえもん',
          previewText: "がおーーー",
          thumbnail: 'https://cdn-ak.f.st-hatena.com/images/fotolife/p/p0lar-star/20110414/20110414102355.jpg'
        },
        {
          id: "6",
          title: 'カバ子と子カバ',
          previewText: "てくてく",
          thumbnail: 'http://www.biopark.co.jp/staff/20110627momokichi1.jpg'
        }
          ]
    }
  },
  // asyncData() {
  //   return new Promise((resolve, reject) => {
  //     setTimeout(() => {
  //       resolve({
  //         recipes: [
  //           {
  //             id: "1",
  //             title: 'カバ蔵',
  //             previewText: "むしゃむしゃ",
  //             thumbnail: 'http://www.tobuzoo.com/zoo/list/details/pc/0_an_21_03.jpg'
  //           },
  //           {
  //             id: "2",
  //             title: 'カバ吉',
  //             previewText: "ぐおーー",
  //             thumbnail: 'https://cdn-ak.f.st-hatena.com/images/fotolife/N/NishImO/20110202/20110202004023.jpg'
  //           },
  //           {
  //             id: "3",
  //             title: 'カバごろう',
  //             previewText: "ぼてっ",
  //             thumbnail: 'https://i.ytimg.com/vi/jYx4qY9ze5o/maxresdefault.jpg'
  //           },
  //           {
  //             id: "4",
  //             title: 'カバ山さん',
  //             previewText: "むーーん",
  //             thumbnail: 'https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Mother_and_very_small_baby_hippo.jpg/200px-Mother_and_very_small_baby_hippo.jpg'
  //           },
  //           {
  //             id: "5",
  //             title: 'カバざえもん',
  //             previewText: "がおーーー",
  //             thumbnail: 'https://cdn-ak.f.st-hatena.com/images/fotolife/p/p0lar-star/20110414/20110414102355.jpg'
  //           },
  //           {
  //             id: "6",
  //             title: 'カバ子と子カバ',
  //             previewText: "てくてく",
  //             thumbnail: 'http://www.biopark.co.jp/staff/20110627momokichi1.jpg'
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