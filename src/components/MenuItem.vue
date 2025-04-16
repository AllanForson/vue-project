<script setup lang="ts">
interface MenuItem {
  text: string
  link: string
}

const menuItems: MenuItem[] = [
  { text: 'Home', link: '/' },
  { text: 'About', link: '/about' },
  { text: 'Contact', link: '/contact' },
]
</script>

<template>
  <header class="header-app">
    <div class="wrapper">
      <nav>
        <ul class="menu">
          <li v-for="item in menuItems" :key="item.text">
            <a :href="item.link">{{ item.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header-app {
  background-color: #333;
  color: white;
  padding: 1rem;
}

.menu {
  list-style: none;
  display: flex;
  gap: 1rem;
  margin: 0;
  padding: 0;
}

.menu li a {
  color: white;
  text-decoration: none;
}

.menu li a:hover {
  text-decoration: underline;
}
</style>
