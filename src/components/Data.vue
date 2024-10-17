<template>
    <H1> Two way Binding:</H1>
    <input type="text" v-model="count"/>
    <h3> {{ count }}</h3>
    <input type="text" placeholder="Enter email" v-model="email" />
    <br/>
    <input type="password" placeholder="enter password" v-model="password"/>
    <br>
    <button v-on:click="getData()" type="button">Get Values</button>
 
 </template>
 
 
 <script>
 export default {
         name: "Data",
         data(){
             return {
                 count:0
                 }
             },
             methods: {
                 getName(name){
                     return name;
                 
             
             },
             return{
                 email:null,
                 password:null,
             }
         },
         methods: {
             getData(){
                 return {
                     name: "Cole",
                     email:this.email
                 }
                 console.warn("values:",this.email,this.password)
             }
             }}
         
     
 </script>
 