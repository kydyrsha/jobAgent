<template>
  <div class="card-wrapper">
    <div class="card">
      <img src="@/assets/img/bank.svg" alt="logo">
      <div class="card-info">
        <h2>Senior Software Developer (Re-advertised)</h2>
        <div class="company-name">
          <p>Company:</p>
          <a href="#">I&M Bank</a>
        </div>
        <div class="location-name">
          <p>Location:</p>
          <a href="#">Nairobi, Kenya</a>
        </div>
        <div class="data">
          <div class="posted">
            <i class="ri-time-line"></i>
            <p>Posted 3 days ago</p>
          </div>
          <div class="views">
            <i class="ri-eye-line"></i>
            <p>420 views</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card.vue"
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
}

.card-wrapper .card .card-info {
  padding:0 0 0 1rem;
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

.card-wrapper .data > div {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-wrapper .data > div > i {
  margin-right: 0.5rem;
}
</style>
