<template>
  <div>
    <form>
      <input type="text" name="busca" id="busca" v-model="busca" />
      {{busca}}
      <router-link  :to="{name: 'Usuario', params: {user: this.busca}}"><img src="@/assets/search.svg" /></router-link>
    </form>
  </div>
</template>

<script>
export default {
  data(){
    return {
      busca: ""
    }
  }
};
</script>

<style scoped>
input {
  background: #ffffff;
  border: 2px solid #000000;
  box-sizing: border-box;
  font-size: 25px;

  width: 500px;
  height: 40px;
}
a {
  background: #000000;
  border-radius: 0px;
  border: none;
  height: 40px;
  width: 80px;
  margin-left: -5px;

  align-items: center;
  display: flex;
  justify-content: center;
}
form {
  display: flex;
}
</style>