<template>
   <H1> Two way Binding:</H1>
   <input type="text" placeholder="Enter email" v-model="email" />
   <br/>
   <input type="password" placeholder="enter password" v-model="password"/>
   <br>
   <button v-on:click="getData()" type="button">Get Values</button>

</template>


<script>
export default {
        name: "Home",
        data(){
            return{
                email:null,
                password:null,

            }
        },
        methods: {
            getData(){
                console.warn("values:",this.email,this.password)

            }
        }
}
    

</script>

<style scoped>

</style>