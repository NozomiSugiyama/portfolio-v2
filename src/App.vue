<template>
  <div id="app">
    <router-view/>
    <link href="https://fonts.googleapis.com/css?family=IBM+Plex+Serif" rel="stylesheet">
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
* {
  margin: 0;
  font-family: 'IBM Plex Serif', serif;
}

#app {
  --app-background-color: #fafbfd;
  background-color: var(--app-background-color);
}

html {
  font-size: 16px;
}

@media (max-width: 1020px) and (min-width: 768px) { 
  html {
    font-size: 14px;
  } 
}


@media (max-width: 767px) {
  html {
    font-size: 10px;
  }
}

</style>
