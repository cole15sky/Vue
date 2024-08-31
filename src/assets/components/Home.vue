<template>
    <h1> Home Component </h1>
    <h1> Mobile: {{ mobile }}</h1>
    <h1>  {{ getName("Peter") }}</h1>
    <h1>  All Date: {{ getData().email }}</h1>
</template>


<script>
export default {
        name: "Home",
        data(){
            return {
                email:'aakash@gmail.com',
                mobile: 12345
                }
            },
            methods: {
                getName(name){
                    return name;
                
            
            },
            getData(){
                return {
                    name: "Cole",
                    email:this.email
                }
            }
            }}
    

</script>

<style scoped>

</style>