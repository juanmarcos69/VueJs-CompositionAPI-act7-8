<script setup>

import PostItem from '@/components/PostItem.vue'
import MyWrapper from '@/components/MyWrapper.vue'


const posts = [
  {
    id: 1,
    title: 'Post Title 1',
    body: 'This is the body of post number 1.',
    author: 'Jeek Ian',
    created_at: '2024-10-01',
    is_saved: false,
  },
  {
    id: 2,
    title: 'Post Title 2',
    body: 'This is the body of post number 2.',
    author: 'Jane Smith',
    created_at: '2024-10-02',
    is_saved: false,
  },
  {
    id: 3,
    title: 'Post Title 3',
    body: 'This is the body of post number 3.',
    author: 'John Doe',
    created_at: '2024-10-03',
    is_saved: false,
  },
  {
    id: 4,
    title: 'Post Title 4',
    body: 'This is the body of post number 4.',
    author: 'Jane Smith',
    created_at: '2024-10-04',
    is_saved: false,
  },
  {
    id: 5,
    title: 'Post Title 5',
    body: 'This is the body of post number 5.',
    author: 'John Doe',
    created_at: '2024-10-05',
    is_saved: false,
  },
  {
    id: 6,
    title: 'Post Title 6',
    body: 'This is the body of post number 6.',
    author: 'Jane Smith',
    created_at: '2024-10-06',
    is_saved: false,
  },
  {
    id: 7,
    title: 'Post Title 7',
    body: 'This is the body of post number 7.',
    author: 'John Doe',
    created_at: '2024-10-07',
    is_saved: false,
  },
  {
    id: 8,
    title: 'Post Title 8',
    body: 'This is the body of post number 8.',
    author: 'Jane Smith',
    created_at: '2024-10-08',
    is_saved: false,
  },
  {
    id: 9,
    title: 'Post Title 9',
    body: 'This is the body of post number 9.',
    author: 'John Doe',
    created_at: '2024-10-09',
    is_saved: false,
  },
  {
    id: 10,
    title: 'Post Title 10',
    body: 'This is the body of post number 10.',
    author: 'Jane Smith',
    created_at: '2024-10-10',
    is_saved: false,
  },
  {
    id: 11,
    title: 'Post Title 11',
    body: 'This is the body of post number 11.',
    author: 'John Doe',
    created_at: '2024-10-11',
    is_saved: false,
  },
  {
    id: 12,
    title: 'Post Title 12',
    body: 'This is the body of post number 12.',
    author: 'Jane Smith',
    created_at: '2024-10-12',
    is_saved: false,
  },
  {
    id: 13,
    title: 'Post Title 13',
    body: 'This is the body of post number 13.',
    author: 'John Doe',
    created_at: '2024-10-13',
    is_saved: false,
  },
  {
    id: 14,
    title: 'Post Title 14',
    body: 'This is the body of post number 14.',
    author: 'Jane Smith',
    created_at: '2024-10-14',
    is_saved: false,
  },
  {
    id: 15,
    title: 'Post Title 15',
    body: 'This is the body of post number 15.',
    author: 'John Doe',
    created_at: '2024-10-15',
    is_saved: false,
  },
  {
    id: 16,
    title: 'Post Title 16',
    body: 'This is the body of post number 16.',
    author: 'Jane Smith',
    created_at: '2024-10-16',
    is_saved: false,
  },
  {
    id: 17,
    title: 'Post Title 17',
    body: 'This is the body of post number 17.',
    author: 'John Doe',
    created_at: '2024-10-17',
    is_saved: false,
  },
  {
    id: 18,
    title: 'Post Title 18',
    body: 'This is the body of post number 18.',
    author: 'Jane Smith',
    created_at: '2024-10-18',
    is_saved: false,
  },
  {
    id: 19,
    title: 'Post Title 19',
    body: 'This is the body of post number 19.',
    author: 'John Doe',
    created_at: '2024-10-19',
    is_saved: false,
  },
  {
    id: 20,
    title: 'Post Title 20',
    body: 'This is the body of post number 20.',
    author: 'Jane Smith',
    created_at: '2024-10-20',
    is_saved: false,
  },
]
</script>

<template>
  <div v-for="post in posts" :key="post.id">
    <MyWrapper>
        <PostItem :post="post"/>
      </MyWrapper>
  </div>
</template>
