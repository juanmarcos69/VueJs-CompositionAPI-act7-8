<script setup>
import { usesPostStore } from '@/stores/posts'

const postStore = usesPostStore()


defineProps({
  post: {
    type: Object,
    required: true
  }
})

</script>

<template>
  <div>
     <div class="header">
        <span>Written by {{ post.author }} on {{ post.created_at }}</span>
        <div class="actions">
          <button @click="postStore.deletePost(post.id)" class="del material-icons">delete</button>
          <button @click="postStore.savePost(post.id)" class="save material-icons">
            {{ post.is_saved ? 'bookmark' : 'bookmark_border' }}
          </button>
        </div>
      </div>
      <h1>{{ post.title }}</h1>
      <p>{{ post.body }}</p>
  </div>
</template>


<style lang="scss" scoped>


  .header {
    font-size: 12px;
    background: #006aff;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #fff;
    font-weight: 300;
    border-top-left-radius: 1rem;
    border-top-right-radius: 1rem;

    .actions {
      display: flex;
      gap: 0.5rem;

      button {
        border: none;
        background: #fff;
        border-radius: 30px;
        font-size: 1.2rem;
        cursor: pointer;
        padding: 0.3rem 0.6rem;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: 0.2s ease-in-out;

        &.del {
          color: #e74c3c;

          &:hover {
            background: #fddede;
            color: #c0392b;
          }
        }

        &.save {
          color: #27ae60;

          &:hover {
            background: #dff5e4;
            color: #1e8449;
          }
        }
      }
    }
  }

  h1 {
    margin-bottom: 0.5rem;
    font-size: 1.5rem;
    color: #333;
  }

  p {
    line-height: 1.6;
    color: #444;
  }

</style>
