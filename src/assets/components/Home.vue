<template>
   <H1> Two way Binding:</H1>
   <input type="text" v-model="count"/>
   <h3> {{ count }}</h3>
</template>


<script>
export default {
        name: "Home",
        data(){
            return {
                count:0
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