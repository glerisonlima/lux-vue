<template>
  <ul>
      <li v-for="repo in dados_repositories" :key="repo.id">
          <h1>{{repo.name}}</h1>
          <p>{{repo.description}}</p>
          <div class="forks">
              <img src="@/assets/star.svg" alt="stars">
              <span>{{repo.forks}}</span>
          </div>
      </li>
  </ul>
</template>

<script>
export default {

    props: {
        dados_repositories: {type: []}
    }
}
</script>

<style scoped>
    li{
        margin-bottom: 30px;
        margin-left: 15px;
    }
    h1{
        font-family: Rubik;
        font-style: normal;
        font-weight: 300;
        font-size: 36px;
        line-height: 43px;
        color: #000000;
    }
    p{
        font-family: Rubik;
        font-style: normal;
        font-weight: 300;
        font-size: 16px;
        line-height: 28px;
        color: #757575;
    }

    img{
        width: 20px;
        height: 20px;
    }

    span{
        font-family: Rubik;
        font-style: normal;
        font-weight: 300;
        font-size: 20px;
        line-height: 24px;
        color: #757575;
        margin-left: 8px;
    }

    .forks{
        display: flex;
        align-items: center;
        margin-top: 10px;
    }
</style>