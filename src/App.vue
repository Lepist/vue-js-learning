<template>
  <div class="App">
    <h4>Название поста</h4>
    <input v-bind:value="title" type="text" placeholder="Название">
    <input v-bind:value="body" @input="input" type="text" placeholder="Описание">
    <button class="btn">Создать</button>
    <div class="post" v-for="post in posts">
      <p><strong>Название: </strong> {{ post.title }}</p>
      <p><strong>Описание: </strong> {{ post.body }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      posts: [
        {id: 1, title: "Название JS", body: "Описание 1"},
        {id: 2, title: "Название JS 2", body: "Описание 2"},
        {id: 3, title: "Название JS 3", body: "Описание 3"},
        {id: 4, title: "Название JS 4", body: "Описание 4"}

      ],
      title: '',
      body: ''
    }
  }
} 
</script>

<style>

</style>