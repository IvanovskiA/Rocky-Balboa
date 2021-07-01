<template>
  <section class="grid-container">
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
import Recipe from '@/components/Recipe';

export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve ({
          recipes: [
            {
              id: "1",
              title: "Rocky I",
              previewText: "1976",
              thumbnail: "https://i.pinimg.com/originals/ec/92/76/ec9276d3087039193e9d543bbb25f77b.jpg"
            },
            {
              id: "2",
              title: "Rocky II",
              previewText: "1979",
              thumbnail: "https://imagesvc.meredithcorp.io/v3/mm/image?url=https%3A%2F%2Fstatic.onecms.io%2Fwp-content%2Fuploads%2Fsites%2F20%2F2019%2F06%2Fmsdrock_ec030.jpg"
            },
            {
              id: "3",
              title: "Rocky III",
              previewText: "1982",
              thumbnail: "https://www.thebioneer.com/wp-content/uploads/2015/03/rocky-sprint-training.jpg"
            },
            {
              id: "4",
              title: "Rocky IV",
              previewText: "1985",
              thumbnail: "https://www.filmstories.co.uk/wp-content/uploads/2020/07/rocky-4-lead-850x600.jpg"
            },
            {
              id: "5",
              title: "Rocky V",
              previewText: "1990",
              thumbnail: "http://archeravenue.net/wp-content/uploads/2020/04/rocky5.jpg"
            },
            {
              id: "6",
              title: "Rocky Balboa",
              previewText: "2006",
              thumbnail: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT52pSzuelHMad5-G5SvxMERxuLUTftfwSJrNpyjl5RoNrDHJhIXQAwJnM1ceVpUU_Tqfs&usqp=CAU"
            },
            {
              id: "7",
              title: "Creed",
              previewText: "2015",
              thumbnail: "https://s.wsj.net/public/resources/images/BN-LK714_creed1_M_20151124114342.jpg"
            },
            {
              id: "8",
              title: "Creed II",
              previewText: "2018",
              thumbnail: "https://api.time.com/wp-content/uploads/2015/11/crd-fp-085r.jpg"
            }
          ]
        })
      }, 1500)
    })
  }
};
</script>

<style scoped>
/* .recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
  text-align: center; 
  width: 320px;
} */

.grid-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 250px;
  grid-gap: 50px;
  width: 320px;
  column-gap: normal;
  justify-content: center;
  text-align: center; 
  margin-left: 715px;
  }
</style>