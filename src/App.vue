<template>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <br>
        <RouterLink to="/about">About</RouterLink>
      </nav>
  <RouterView />
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'

</script>
