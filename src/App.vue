<template>
  <div id="app">
    <Header></Header>
    <Search
        :searchKey="searchKey"
        :onChange="onChange"
        :onSort="onSort"
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
      searchKey: '',
      sortByViews: false,
    }
  },
  computed: {
    jobList() {
      if (this.searchKey) {
        return this.jobs.filter(job => (job.name.toLowerCase().includes(this.searchKey.toLowerCase())))
      }
      if (this.sortByViews) {
        let j = [...this.jobs]
        return j.sort(function (a, b) {
         return b.views - a.views
        })
      }
      return this.jobs
    }
  },
  methods: {
    onChange(e) {
      this.searchKey = e.target.value
    },
    onSort(isSort) {
      this.sortByViews = isSort
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
