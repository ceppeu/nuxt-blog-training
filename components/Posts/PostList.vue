<template>
  <section class="posts-list">
      <PostPreview
        id="1"
        :is-admin="isAdmin"
        thumbnail="https://lock0.files.wordpress.com/2010/03/genialo.png"
        title="Hola Mundo"
        previewText="Descripción de Hola Mundo"
      />
    </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'

export default {
  name: 'PostList',
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style>

.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

</style>