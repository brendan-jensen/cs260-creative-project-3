<template>
<div class="wrapper">
  <div class="posts">
    <div class="post" v-for="post in posts" :key="post.id">
      <div class="header">
        <h2>{{post.title}}</h2>
        <p><i>{{post.time}}</i></p>
      </div>
      <div class="info">
        <p>{{post.text}}</p>
      </div>
      <br>
      <hr>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'PostsView',
  props: {
    posts: Array
  }
}
</script>

<style scoped>
.wrapper {
  text-align: left;
}
/* .wrapper {
  display: flex;
  align-items: center;
  justify-content: left;
}

.posts {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.post {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
  text-align: left;
} */
</style>