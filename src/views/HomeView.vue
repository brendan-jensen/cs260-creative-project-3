<template>
  <div>
    <div class="wrapper">
      <h2>What's on your mind?</h2>
      <div class="add">
        <div class="form">
          <input v-model="title" placeholder="Your title here" />
          <p></p>
          <textarea v-model="text" placeholder="Your text here" />
          <p></p>
          <button @click="upload">Upload</button>
        </div>
      </div>
    </div>
    <PostsView :posts="posts" />
  </div>
</template>

<<script>
import PostsView from "../components/PostsView.vue";
import moment from 'moment';

export default {
  name: 'Home',
  components: {
    PostsView,
  },
  data() {
    return {
      title: "",
      text: "",
    }
  },
  computed: {
    posts() {
      return this.$root.$data.posts;
    }
  },
  methods: {
    upload() {
        this.$root.$data.posts.push({
          title: this.title,
          text: this.text,
          time: moment().format('MMMM Do YYYY, h:mm:ss a')
        });
        this.title = "";
        this.text = "";
    },
  },
}
</script>
