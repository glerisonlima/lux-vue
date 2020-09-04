<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700;900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@300&display=swap");
body,
ul,
li,
h1,
h2,
p {
  padding: 0;
  margin: 0;
}

html,
body {
  height: 100%;
  min-height: 100%;
}

body {
  font-family: "Roboto", sans-serif;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>
