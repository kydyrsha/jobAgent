<template>
  <div class="card-wrapper">
    <div class="card" v-for="(job, index) in jobs" :key="index">
      <img src="@/assets/img/bank.svg" alt="logo">
      <div class="card-info">
        <h2>{{job.name}}</h2>
        <div class="card-link company-name">
          <p>Company:</p>
          <a href="#">{{job.company}}</a>
        </div>
        <div class="card-link location-name">
          <p>Location:</p>
          <a href="#">{{job.location.city}}, {{job.location.country}}</a>
        </div>
        <div class="data">
          <div class="posted">
            <i class="ri-time-line"></i>
            <p>Posted {{job.postedDaysAgo}} days ago</p>
          </div>
          <div class="views">
            <i class="ri-eye-line"></i>
            <p>{{job.views}} Views</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card.vue",
  props: {
    jobs: Array
  }
}
</script>

<style scoped>

.card-wrapper {
  padding:2rem 0;
}

.card-wrapper .card {
  display: flex;
  align-items: flex-start;
  padding:1rem;
  box-shadow: 0px 4px 8px rgba(33, 33, 33, 0.16);
  border-radius: 8px;
  margin-bottom: 1rem;
  justify-content: space-evenly;
}

.card-wrapper .card > img {
  width:15%;
}

.card-wrapper .card .card-info {
  padding:0 0 0 1rem;
  width:80%;
}
.card-wrapper .card .card-info .card-link > a {
  color:#CD6405;
}
.card-wrapper .card .card-info > h2 {
  margin-bottom: 1rem;
  text-transform: uppercase;
}

.card-wrapper .company-name, .location-name {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5rem;
}

.card-wrapper .data {
  display: flex;
  justify-content: space-between;
  margin-top: 1rem;
}

.card-wrapper .data  p {
  font-size: 12px;
}

.card-wrapper .data > div {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-wrapper .data > div > i {
  margin-right: 0.5rem;
}


</style>
