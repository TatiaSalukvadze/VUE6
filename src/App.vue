<template>
    <user-data @current-user="currentUser"></user-data>
    <active-user :name="name" :age="age"></active-user>
</template>
<script>
export default {
   data(){
        return{
            name: '',
            age: ''
        };
    },
    methods:{
        currentUser(name,age){
            this.name = name;
            this.age = age;
        }
    }
}
</script>

<style>
#app{
    display:flex;
}
#hs, form{
    flex:5;
    padding-top:20vh;
}
#hs{
    padding-right:25vw;
}
form{
    padding-left:25vw;
}

</style>
