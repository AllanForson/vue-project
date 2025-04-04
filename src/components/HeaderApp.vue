<script setup lang="ts">
import { ref } from 'vue'

interface MenuItem {
  text: string
  link: string
}
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <ul>
          <li v-for="item in menuItems" :key="item.text">
            <a :href="item.link">{{ item.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
