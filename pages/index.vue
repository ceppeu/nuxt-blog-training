<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get te latest tech news</h1>
    </section>
      <PostList
        id="1"
        thumbnail="https://lock0.files.wordpress.com/2010/03/genialo.png"
        title="Hola Mundo"
        previewText="Descripción de Hola Mundo"
      />
  </div>
</template>

<script>
import PostList from '~/components/Posts/PostList'

export default {
  components: {
    PostList
  }
}
</script>

<style>

.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
  background-image: url('~assets/images/main-page-background.jpg')
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

</style>