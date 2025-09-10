<template>
  <div class="wrapper">
    <slot></slot>
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
}

  </style>
