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
      ],

      myObjects:[
        { 
          title: "Blue is a color",
          No: 9836363633,
          location: "Tadi"
        },
        { 
          title: "Black is a color",
          No: 9836660633,
          location: "Tadi"
        },
      ]


    }
  }
}
</script>


<template>
  <div>

  <ul>
    <li v-for="({title,No},index) in myObjects">
     {{ index +1  }} <br>
     {{ title }} <br>
     {{ No }}

   </li>
  </ul>
</div>


  <div v-for="(book, index) in books">
    <h2>book {{ index + 1  }}     </h2>
    <h1> {{ book.name }}</h1>
    <h2> {{ book.Author }}</h2>
    <h1> {{ book.Price }}</h1>
  </div>

</template>