<template>
  <div class="row">
    <div class="card">
      <div class="card-body">
    <h5 class="card-title">Books</h5>
    <a href="#" class="btn btn-primary" style="margin:5px;" @click="createBook()">Ajouter</a>
    <a href="#" class="btn btn-primary" @click="showBooksList()">Modifier & supprimer</a>
  </div>
    </div>
    <div class="card">
      <div class="card-body">
    <h5 class="card-title">Genre</h5>
    <a href="#" class="btn btn-primary" @click="createGenre()">Ajouter</a>
  </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BooksAdmin',
  methods: {
    createBook(){
      this.$router.push({name:'adminBooksAction'}).catch(error =>{console.log('erreur de navigation' + error)});
    },
    showBooksList(){
      this.$router.push({path: '/admin/bookslist'}).catch(error =>{console.log('erreur de navigation' + error)});
    },
    createGenre(){
      this.$router.push({path: '/admin/genres'}).catch(error =>{console.log('erreur de navigation' + error)});
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
        margin: 0 auto; /* Added */
        float: none; /* Added */
        margin-bottom: 10px; /* Added */
}
</style>