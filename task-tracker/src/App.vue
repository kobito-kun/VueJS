<template>
  <div>
    <Header msg="Todo List! " />
  </div>
</template>

<script>
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    Header,
  }
}
</script>

<style>
div{
  text-align: center;
  display: grid;
  place-items: center;
}
</style>