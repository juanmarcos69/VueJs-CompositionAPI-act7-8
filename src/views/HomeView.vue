<script setup>
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
    <div class="wrapper">
      <div class="header">
        <span>Written by {{ post.author }} on {{ post.created_at }}</span>
        <div class="actions">
          <button class="del"><span class="material-icons">delete</span></button>
          <button class="save"><span class="material-icons">bookmark_border</span></button>
        </div>
      </div>
      <h1>{{ post.title }}</h1>
      <p>{{ post.body }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  margin: 2rem;
  background: #fff;
  box-shadow:
    rgba(0, 0, 0, 0.1) 0px 1px 10px -3px,
    rgba(0, 0, 0, 0.1) 0px 4px 6px -2px;
  border-radius: 1rem;
  overflow: hidden;
  padding: 1.5rem;

  .header {
    font-size: 12px;
    background: #0288d1;
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
}
</style>
