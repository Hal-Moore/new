<template>
    <main class="content">
    <div class="page-title">
        <h4>Категории</h4>
        <router-link to="/new" tag="button" class="waves-effect waves-light btn grey darken-1">Добавить категорию</router-link>
    </div>


    <div  class="row">
        <div  class="col s12">
            <div v-for="post in categories" :key="post.id" class="collection">
                <a href="#!" class="collection-item">{{post.name}}</a>
            </div>
        </div>
    </div>
</main>

</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      categories: [],
      errors: []
    }
  },
  created() {
      axios.get('/categories')
      .then(response=>{
          this.categories = response.data
      })
        .catch(e => {
        this.errors.push(e)
    }) 
  },
}

</script>