<template>
<div class="search-wrapper">
  <h2>JOB SEARCH</h2>
  <div class="input-wrapper">
    <input type="text" placeholder="Search">
    <img src="@/assets/img/filter.svg" alt="filter-icon">
  </div>
  <div class="filter-wrapper">
    <p>Sort by:</p>
    <p>Views <i class="ri-arrow-down-s-line"></i></p>
  </div>
</div>
</template>

<script>
export default {
  name: "Search.vue"
}
</script>

<style scoped>

.search-wrapper > h2 {
  margin-bottom: 1rem;
}
.search-wrapper .input-wrapper > input {
  width:100%;
  max-width: 80%;
}

.search-wrapper .input-wrapper > input:focus {
  border-width: 0;
}
.search-wrapper .input-wrapper > img {
  padding:1rem;
  background-color: #FFC803;
  border-radius: 8px;
  cursor: pointer;
  opacity:0.8;
  transition: 0.6s;
}

.search-wrapper .input-wrapper > img:hover {
  opacity:1;
}

.search-wrapper .input-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: initial;
  margin-bottom: 0.5rem;
}

.search-wrapper .filter-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.search-wrapper .filter-wrapper > p:nth-child(2) {
  display: flex;
  align-items: center;
}
</style>
