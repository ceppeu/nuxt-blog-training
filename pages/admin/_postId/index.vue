<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'

export default {
  layout: 'admin',
  components: {
    AdminPostForm
  },
  data: function () {
    return {
      loadedPost: {
        author: 'Agustin Torres',
        title: 'AWESOME',
        content: 'Magic content for post',
        thumbnailLink: 'https://lock0.files.wordpress.com/2010/03/genialo.png'
      }
    }
  }
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>