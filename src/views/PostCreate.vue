<script setup>
import { reactive, computed } from 'vue'
import { usesPostStore } from '@/stores/posts'
import { useRouter } from 'vue-router';
import MyWrapper from '@/components/MyWrapper.vue'

const postStore = usesPostStore()

const router = useRouter()
const post = reactive({
  title: '',
  body: ''
})

const isFormInvalid = computed(() => {
  return post.title === '' || post.body === ''
})

const submit = () => {
  postStore.addPost(post)
  router.push({ name: 'home' })
}
</script>

<template>
  <MyWrapper>
    <form @submit.prevent="submit">
      <!-- h3 behaves like a placeholder -->
      <h3 v-if="!post.title && !post.body" class="placeholder-heading">
        📝 Create a new post
      </h3>

      <div>
        <label>Post Title</label>
        <input
          type="text"
          v-model="post.title"
          placeholder="Enter your post title here..."
        />
      </div>

      <div>
        <label>Post Body</label>
        <textarea
          rows="7"
          v-model="post.body"
          placeholder="Write something interesting..."
        ></textarea>
      </div>

      <div>
        <button :disabled="isFormInvalid">Add</button>
      </div>
    </form>
  </MyWrapper>
</template>

<style lang="scss" scoped>
.placeholder-heading {
  font-weight: 400;
  color: #9ca3af; // gray-400
  font-style: italic;
  margin-bottom: 1rem;
}

div {
  margin-bottom: 1rem;

  label {
    font-weight: 300;
    display: block;
    margin-bottom: 0.5rem;
  }

  input,
  textarea {
    max-width: 100%;
    width: 100%;
    border: 1px solid #333;
    padding: 5px;
    border-radius: 5px;

    &:focus {
      outline: 2px solid #333;
      border: none;
    }
  }

  button {
    background: #3b82f6;
    color: #fff;
    width: 101%;
    padding: 5px;
    border-radius: 5px;
    transition: background 0.2s ease;

    &:hover {
      background: #2563eb;
    }

    &:disabled {
      background: #eee;
      cursor: not-allowed;
    }
  }
}
</style>
