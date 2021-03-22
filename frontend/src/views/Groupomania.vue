<template>
    <div>
        <div id="app">
            <NewPost />
            <Post />
        </div>
    </div>
</template>

<script>
import NewPost from '../components/NewPost.vue'
import Post from '../components/Post.vue'
export default {
  name: 'app',
  components: {
    NewPost,
    Post
  }
}
</script>
