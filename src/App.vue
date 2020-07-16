<template>
  <div id="app" :class="{ light: theme === 'light', dark: theme === 'dark' }">
    <p>{{ this.theme }} theme</p>
    <button @click="toggleTheme">Toggle Theme</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      theme: 'light',
    }
  },
  methods: {
    toggleTheme() {
      if (this.theme === 'light') {
        this.theme = 'dark'
      } else {
        this.theme = 'light'
      }
    },
  },
}
</script>

<style lang="scss" scoped>
#app.light {
  --bg-color: white;
  --text-color: black;
}

#app.dark {
  --bg-color: black;
  --text-color: white;
}

#app {
  color: var(--text-color);
  background-color: var(--bg-color);
}
</style>
