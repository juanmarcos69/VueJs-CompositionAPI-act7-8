<script setup>

import PostItem from '@/components/PostItem.vue'
import MyWrapper from '@/components/MyWrapper.vue'
import { usesPostStore } from '@/stores/posts'

const postStore = usesPostStore()


</script>

<template>
  <div v-for="post in postStore.posts" :key="post.id">
    <MyWrapper>
        <PostItem :post="post" />
      </MyWrapper>
  </div>
</template>
