<template>
   

    <div v-for="book of books" :key="book.id">
            <SingleBook :book=book />
    </div>

</template>

<script>

import SingleBook from './SingleBook.vue'
export default{
    name: 'BookBox',
    props:{
        books: Array
    },
    components:{
        SingleBook
    }
}

</script>

<style scoped>

</style>