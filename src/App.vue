<template>
  <div id="app">
    <h1 class="appTitle mt-3">La mejor To-do List App en el mundo mundial</h1>
    <Form></Form>
    
  </div>
</template>

<script>
import Form from './components/Form.vue';

export default {
  name: 'App',
  components: {Form},
}
</script>

<style>
  .appTitle {
    text-align: center;
  }
  .listTitle {
    text-align: center;
  }
</style>
