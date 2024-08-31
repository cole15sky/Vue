<template>
  <h1> Get checkbox & Radio Button Value</h1>
  <h3> Technology</h3>
  <label for="Javascript">Javascript</label>
<input type="checkbox" value="Javascript" v-model="technology" id="Javascript">

  <label for="Python">Python</label>
<input type="checkbox" value="Python" v-model="technology" id="Python">
<h4> Selected  Technology :{{technology}}</h4>


</template>


<script>
export default {
        name: "Home",
        data(){
            return{
                technology:[]

            }
        },
    }
          

</script>

<style scoped>

</style>