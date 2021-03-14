<template>
  <div id="app">
    <NavBar />
    <AddComment />
    <AddLike />
    <DeleteButton />
    <Footer />
    <NewPost />
    <PostList />
    <SignOut />
    <b-container>
      <router-view/>
    </b-container>
  </div>
</template>

<script>
import AddComment from './components/AddComment.vue'
import AddLike from './components/AddLike.vue'
import DeleteButton from './components/DeleteButton.vue'
import Footer from './components/Footer.vue'
import NavBar from './components/NavBar.vue'
import NewPost from './components/NewPost.vue'
import PostList from './components/PostList.vue'
import SignOut from './components/SignOut.vue'

export default {
  name: 'app',
  components: {
    AddComment,
    AddLike,
    DeleteButton,
    Footer,
    NavBar,
    NewPost,
    PostList,
    SignOut
  }
}

</script>

<style lang = scss>
 #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

#logo{
    max-width: 35%;
    height: auto;
}
</style>
