<template>
  <div id="app">
    <Header></Header>
    <Search></Search>
    <Card></Card>
  </div>
</template>

<script>

import Header from '@/components/Header';
import Search from '@/components/Search';
import Card from '@/components/Card';

export default {
  name: 'App',
  components: {
    Header,
    Search,
    Card
  }
}
</script>

<style>

* {
  box-sizing: border-box;
  margin:0;
  font-size: 16px;
}

#app {
  width:100%;
  max-width:375px;
  margin:0 auto;
  display: block;
}
</style>
