<template>
  <div class="detalhe">
    <div class="busca">
    <h1>Github <span>Search</span></h1>
    <SearchBar />
    </div>
    <div class="main">
    <UsuarioDetalhe :dados_usuario="dados" />
    <UsuarioRepositories :dados_repositories="repositories"/>
    </div>
  </div>
</template>



<script>
import UsuarioDetalhe from "@/components/UsuarioDetalhe.vue";
import UsuarioRepositories from "@/components/UsuarioRepositories.vue";
import SearchBar from "@/components/SearchBar.vue";

import { api } from "@/services.js";

export default {
  components: {
    UsuarioDetalhe,
    UsuarioRepositories,
    SearchBar
  },

  data() {
    return {
      usuario: "",
      dados: [],
      repositories: []
    };
  },

  

  methods: {
    getUsuario() {
      api.get(this.usuario).then((resp) => {
        this.dados = resp.data;
      });
    },
    getRepositories(){
      api.get(this.usuario+"/repos").then((resp) => {
        this.repositories = resp.data;
      })
    }
  },

  created() {
    if (this.$route.params.user) {
      this.usuario = this.$route.params.user;
      this.getUsuario();
      this.getRepositories();
    }
  },
};
</script>

<style>
.detalhe{
  display: flex;
  flex-direction: column;
}
.main{
  display: flex;
}
.busca{
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 15px;
}

.busca > h1 {
  font-style: normal;
  font-weight: bold;
  font-size: 30px;
  line-height: 40px;

  color: #000000;
}
.busca > h1 > span {
  font-weight: lighter;
}
</style>
