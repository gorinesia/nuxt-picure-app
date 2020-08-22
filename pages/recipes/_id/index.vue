<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  // data(context) {
  //   return {
  //     recipe: [
  //       {
  //         id: "1",
  //         title: 'Amazing Sushi',
  //         previewText: "Beautiful Sushi plates!!",
  //         descriptionText: 'This is really a delicious meal!!',
  //         thumbnail: 'http://www.atpress.ne.jp/releases/52102/img_52102_1.jpg'
  //       },
  //       {
  //         id: "2",
  //         title: 'Delicious Sushi',
  //         previewText: "Awesome Sushi!!",
  //         descriptionText: 'This is really a delicious meal!!',
  //         thumbnail: 'https://i.ytimg.com/vi/UGJ11p6MHNI/maxresdefault.jpg'
  //       }
  //     ].find(el => el.id === context.params.id)
  //   }
  // },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: 'Amazing Sushi',
              previewText: "Beautiful Sushi plates!!",
              descriptionText: 'This is really a delicious meal!!',
              thumbnail: 'http://www.atpress.ne.jp/releases/52102/img_52102_1.jpg'
            },
            {
              id: "2",
              title: 'Delicious Sushi',
              previewText: "Awesome Sushi!!",
              descriptionText: 'This is really a delicious meal!!',
              thumbnail: 'https://i.ytimg.com/vi/UGJ11p6MHNI/maxresdefault.jpg'
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.single-recipe {
  display: flex; 
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}

.recipe-image {
  width: 80%;
  height: 400px;
}
</style>