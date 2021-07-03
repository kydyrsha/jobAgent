<template>
  <div id="app">
    <Header></Header>
    <Search
        :searchKey="searchKey"
        :onChange="onChange"
    />
    <Card :jobs="jobList" />
  </div>
</template>

<script>

import Header from '@/components/Header';
import Search from '@/components/Search';
import Card from '@/components/Card';
import json from '../data/jobs-mock.json'

export default {
  name: 'App',
  components: {
    Header,
    Search,
    Card
  },
  data() {
    return {
      jobs: json.jobs,
      searchKey: ''
    }
  },
  computed: {
    jobList() {
      if (this.searchKey) {
        return this.jobs.filter(job => (job.name.toLowerCase().includes(this.searchKey.toLowerCase())))
      }
      return this.jobs
    }
  },
  methods: {
    onChange(e) {
      this.searchKey = e.target.value
    }
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;1,700&display=swap');

* {
  box-sizing: border-box;
  margin:0;
  font-size: 16px;
  font-family: 'Roboto', sans-serif;
}

#app {
  width:100%;
  max-width:375px;
  margin:0 auto;
  display: block;
}
</style>
