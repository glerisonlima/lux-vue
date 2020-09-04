<template>
  <div class="dados-usuario">
    <div class="avatar">
      <img :src="dados_usuario.avatar_url" alt="avatar" />
      <h1>{{dados_usuario.name}}</h1>
      <p>{{dados_usuario.login}}</p>
    </div>
    <ul>
      <li>
        <img src="@/assets/organization.svg" alt="organization" />
        <p>{{dados_usuario.company}}</p>
      </li>
      <li>
        <img src="@/assets/location.svg" alt="location" />
        <p>{{dados_usuario.location}}</p>
      </li>
      <li>
        <img src="@/assets/star.svg" alt="star" />
        <p>{{dados_usuario.followers}}</p>
      </li>
      <li>
        <img src="@/assets/repository.svg" alt="repository" />
        <p>{{dados_usuario.public_repos}}</p>
      </li>
      <li>
        <img src="@/assets/followers.svg" alt="followers" />
        <p>{{dados_usuario.following}}</p> 
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    dados_usuario: {type: []},
  },
};
</script>

<style>
.dados-usuario {
  display: flex;
  flex-direction: column;
  padding: 15px;
  min-width: 300px;
}

.avatar img {
  width: 300px;
  height: 300px;
  border-radius: 2px;
  filter: drop-shadow(0px 0px 4px #000000);
}

.avatar h1 {
  font-family: Rubik;
  font-style: normal;
  font-weight: 300;
  font-size: 36px;
  line-height: 43px;
  color: #000000;
}

.avatar p {
  font-family: Rubik;
  font-style: normal;
  font-weight: 300;
  font-size: 24px;
  line-height: 28px;

  color: #757575;
}

.dados-usuario ul {
  margin-top: 44px;
}

.dados-usuario li {
  display: flex;
  align-items: center;
  margin: 10px 0px;
}

.dados-usuario li img {
  width: 20px;
  height: 15px;
  left: 2px;
  top: 6px;
}

.dados-usuario li p {
  font-family: Rubik;
  font-style: normal;
  font-weight: 300;
  font-size: 20px;
  line-height: 24px;
  color: #757575;
  margin-left: 12px;
}
</style>