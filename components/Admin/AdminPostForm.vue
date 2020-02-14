<template>
  <form @submit.prevent="onSave">
    <AppControlInput v-model="editedPost.author">Author Name</AppControlInput>
    <AppControlInput v-model="editedPost.title">Title</AppControlInput>
    <AppControlInput v-model="editedPost.thumbnail">Image</AppControlInput>
    <AppControlInput
      control-type="textarea"
      v-model="editedPost.previewText">Preview Text</AppControlInput>
    <AppControlInput
      control-type="textarea"
      v-model="editedPost.content">Content</AppControlInput>
      <AppButton type="submit">Save</AppButton> 
      <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel">Cancel</AppButton> 
  </form>
</template>

<script>
import AppControlInput from '@/components/UI/AppControlInput'
import AppButton from '@/components/UI/AppButton'

export default {
  name: 'AdminPostForm',
  components: {
    AppButton,
    AppControlInput
  },
  props: {
    post: {
      type: Object,
      required: true
    }
  },
  data: function () {
    return {
      editedPost: this.post
      ? { ...this.post }
      : {
        author: '',
        title: '',
        content: '',
        thumbnail: '',
        previewText: ''
      }
    }
  },
  methods: {
    onSave: function () {
      this.$emit('submit', this.editedPost)
    },
    onCancel: function () {
      this.$router.replace('/admin')
    }
  }
}
</script>