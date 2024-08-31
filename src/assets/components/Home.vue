<template>
    <h1> Home Component </h1>
    <h1> Mobile: {{ mobile }}</h1>
    <h1>  {{ getName() }}</h1>
</template>


<script>
export default {
        name: "Home",
        data(){
            return {
                email:'aakash@gmail.com',
                mobile: 12345,
                getName: function()
                {
                    return "Madoona: True Blue"
                }

                }
            }
        }
    

</script>

<style scoped>

</style>