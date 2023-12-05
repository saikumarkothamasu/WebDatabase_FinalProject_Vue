<template>
    <div>
        <h2> {{bookName}}</h2>
        <h2>{{authorName}} </h2>
        
    </div>
</template>

<script>

    export default{
        name: 'MyHeader',
        props:{
            authorName: String,
            bookName: String
        }

    }
 
</script>

<style scoped>
    div{
        text-align: center;
    }
</style>
