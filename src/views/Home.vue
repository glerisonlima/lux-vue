<template>
  <div class="home">
    <HomeComponent />
    <SearchBar />
  </div>
</template>

<style scoped>
.home {
  height: 100vh;
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>

<script>
import HomeComponent from "@/components/HomeComponent.vue";
import SearchBar from "@/components/SearchBar.vue";

export default {
  name: "Home",
  components: {
    HomeComponent,
    SearchBar,
  },
};
</script>
