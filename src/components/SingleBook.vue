<template>
    <div :class="book.published ? 'green': 'red' ">
                <h1>{{book.day}}</h1>
                <h4>Workout Category : {{book.category}}</h4>
                <h2>Muscle Target : {{book.Exercise_Title}}</h2>
                <h2>Intensity : {{book.Intensity_Level}}</h2>
                <h2>Sets : {{book.sets}}</h2>
                <h2>Reps : {{book.reps}}</h2>
                <h2>Rest Time : {{book.resttime}}</h2>
                <img :src="book.pic" alt="image alt" style="max-width: 20%;">
                
    </div>
</template>

<script>
export default{
    name: 'SingleBook',
    props:{
        book: Array
    }
} 
</script>

 

<style scoped>
.green{
  background-color: rgb(0, 98, 128);
}
h2{
    font-size: 1em;
}
h4{
  margin: 2px
}
div{
  background-color: #FFB89e;
  color: black;
  padding: 1em;
  text-align: center;
  margin: 1em;
}

.red{
  background-color: rgb(0, 208, 255) !important;
}
</style>
