<template>
  
  <!-- Step 3: use the component -->
  <MyHeader bookName="Game of Thrones" authorName ="George RR Martins" />
  <BookBox :books=books />
</template>

<script>
// STep 1 : you import the component
import MyHeader from './components/MyHeader.vue'
import BookBox from './components/BookBox.vue'


export default{
  name: 'App',
  // Step 2: register the component
  components:{
    MyHeader,
    BookBox 
  },
  data(){
    return {
      books: []
    }
  },
  methods:{
    
    async fetchbooks(){
      const res = await fetch("https://ill-erin-mite-tam.cyclic.app/api")
      const data = await res.json()
      console.log(data)
      return data
    }

  },
  async created(){
    this.books = await this.fetchbooks()
  }





}

</script>

<style >

</style>