<script setup>
import { ref } from 'vue'
import { usesPostStore } from '@/stores/posts'
import PostItem from '@/components/PostItem.vue'
import MyWrapper from '@/components/MyWrapper.vue'

const postStore = usesPostStore()
const postFilter = ref('all') // 'all' or 'saved'

// toggle filter
const setPostFilter = () => {
  postFilter.value = postFilter.value === 'all' ? 'saved' : 'all'
}
</script>

<template>
  <div class="header">
    <div>
      <h3>{{ postFilter === 'all' ? 'All posts' : 'Saved posts' }}</h3>
    </div>
    <button
      class="save-btn"
      :class="{ saved: postFilter === 'saved' }"
      @click="setPostFilter"
    >
      {{ postFilter === 'all' ? 'Show saved posts' : 'Show all posts' }}
    </button>
  </div>

  <div v-for="post in postStore.sorted" :key="post.id">
    <MyWrapper>
      <PostItem :post="post" />
    </MyWrapper>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
}

/* Default button style (All posts) */
.save-btn {
  background: linear-gradient(135deg, #007bff, #0056b3);
  color: #fff;
  font-weight: 600;
  border: none;
  padding: 8px 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
}

.save-btn:hover {
  background: linear-gradient(135deg, #0056b3, #004095);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

.save-btn:active {
  transform: translateY(0);
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
}

/* Alternate style when showing saved posts */
.save-btn.saved {
  background: linear-gradient(135deg, #28a745, #1e7e34);
}

.save-btn.saved:hover {
  background: linear-gradient(135deg, #1e7e34, #155d27);
}
</style>
