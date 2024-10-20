<script>
export default {
  data() {
    return {

      books: [{
        name: "From Death",
        Author: "leo nardo ",
        Price: "255$"
      },
      {
        name: "From LIFE",
        Author: "leo nardo de caprico ",
        Price: "315$"
      },
      {
        name: "From Heaven",
        Author: "leo de vinci ",
        Price: "185$"
      },
      ]


    }
  }
}
</script>


<template>

  <div v-for="(book, index) in books">
    <h2>book {{ index + 1  }}     </h2>
    <h1> {{ book.name }}</h1>
    <h2> {{ book.Author }}</h2>
    <h1> {{ book.Price }}</h1>
  </div>

</template>