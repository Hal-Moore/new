<template>
<main class="content">
    <div class="page-title">
        <h4>
            <router-link to="/categories">Категории</router-link>
            <i class="material-icons">keyboard_arrow_right</i>
            Добавить категорию
        </h4>
        <span>
            <button class="btn btn-small red">
              <i class="material-icons">delete</i>
            </button>
          </span>
    </div>

    <div class="row">
        <form v-on:submit="submitCategory()" class="col s12 l6">
            <div class="input-field">
                <input id="name" type="text" v-model="posts.title">
                <label for="name">Название</label>
            </div>
            <div>
                <button class="waves-effect waves-light btn orange lighten-2 mb2">
                    <i class="material-icons left">backup</i>
                    Загрузить изображение
                </button>
            </div>
           

            <div>
                <button class="waves-effect waves-light btn">
                    Сохранить изменения
                </button>
            </div>
        </form>

        <div class="col s12 l4 center">
            <img class="responsive-img" style="height: 200px" src="js/assets/img/no-photo.jpg">
        </div>
    </div>

    <div class="row">
        <div class="col s12">
            <div class="page-subtitle">
                <h4>Позиции:</h4>
                <button class="waves-effect waves-light btn grey darken-1  btn-small modal-trigger " data-target="create-modal">
                    Добавить позицию
                </button>
            </div>

            <div class="collection">
                <a class="collection-item collection-item-icon">
                    <span>
                        Кофе <strong>20 руб.</strong>
                    </span>
                    <span>
                        <i class="material-icons">delete</i>
                    </span>
                </a>
            </div>
        </div>
    </div>


</main>

</template>
<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      posts: {
          title:'',
      },
      errors: []
    }
  },
  methods:{
  submitCategory() {
    axios.post(`/add-category`, this.posts)
    .then(response => {
        console.log(response)
        this.$router.push({path:'/'})
      this.posts = response.data
    })
    .catch(e => {
      this.errors.push(e)
    }) 
  },

  }
}
</script>