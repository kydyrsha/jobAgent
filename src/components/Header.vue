<template>
  <div class="header-wrapper">
    <a href="#"><span>job</span>Agent</a>
    <img src="@/assets/img/profile.svg" alt="">
  </div>
</template>

<script>
export default {
  name: "Header.vue"
}
</script>

<style scoped>
.header-wrapper {
  width:100%;
  max-width:60%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-left: auto;
  padding:1rem 0;
}

.header-wrapper > img {
  width:30px;
  height:auto;
}

.header-wrapper > a {
  text-decoration: none;
  font-style: italic;
  font-size: 20px;
}

.header-wrapper > a > span {
  color: #EEAB02;
  font-style: normal;
  font-size: 20px;
  font-weight: bold;
}
</style>
