<template>
    <form @submit.prevent="sendUser">
        <label>Name:</label><br />
        <input type="text" v-model="name" pattern="[A-Z][a-z]*" required/><br/>
        <label>Age:</label><br/>
        <input type="number" v-model="age" required/><br />
        <button type="submit">Submit</button>
    </form>
</template>

<script>
export default {
    emits:['current-user'],
   data(){
        return{
            name: '',
            age: ''
        };
    },
    methods:{
        sendUser(){

            this.$emit('current-user', this.name,this.age);
          
            this.name = '';
            this.age = '';
        }
    }
}
</script>


<style>
 form{
    width:50vw;
 }
</style>