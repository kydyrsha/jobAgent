<template>
<div class="search-wrapper">
  <h2>JOB SEARCH</h2>
  <div class="input-wrapper">
    <input type="text" placeholder="Search" :value="searchKey" @input="onChange">
    <img src="@/assets/img/filter.svg" alt="filter-icon">
  </div>
  <div class="filter-wrapper">
    <p><b>Sort by:</b></p>
    <div class="sort dropdown">
      <div class="dropbtn"><span>views</span> <i class="ri-arrow-down-s-line"></i></div>
      <div class="dropdown-content">
        <a>popular</a>
        <a>all</a>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "Search.vue",
  props: {
    searchKey: String,
    onChange: Function
  }
}
</script>

<style scoped>

.search-wrapper > h2 {
  margin-bottom: 1rem;
}
.search-wrapper .input-wrapper > input {
  width:100%;
  max-width: 80%;
  padding:0rem 1rem;
  border-radius: 8px;
  background-color: #EAEAEA;
  border-style: none;
}

.search-wrapper .input-wrapper > input:focus {
  outline: none;
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

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  right: 0;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #f1f1f1;}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  cursor: pointer;
}

.dropbtn {
  display: flex;
  align-items: center;
}
</style>
