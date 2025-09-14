<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { Home, PlusCircle } from 'lucide-vue-next'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/" class="nav-link">
        <Home class="icon" /> Home
      </RouterLink>
      <RouterLink to="/post-create" class="nav-link">
        <PlusCircle class="icon" /> New Post
      </RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style lang="scss" scoped>
nav {
  background: #006aff; /* dark gray */
  padding: 1rem 2rem;


  .nav-link {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    color: #f9fafb; /* almost white */
    text-decoration: none;
    margin-right: 1rem;
    padding: 5px 15px;
    border-radius: 5px;
    transition: all 0.2s ease-in-out;

    &:hover {
      background: #5b5d5b00; /* lighter gray */
      color: #60a5fa;     /* nice blue accent */
    }
  }

  .icon {
    width: 18px;
    height: 18px;
  }
}


</style>
