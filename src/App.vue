<template>
    <SkillsComponent/>
</template>

<script>
import SkillsComponent from './components/SkillsComponent.vue';

export default {
  name: 'App',
  components: {
    SkillsComponent
  }
}
</script>

<style >
  @import url('https://fonts.googleapis.com/css?family=Montserrat:400,700');

  body {
    background-color: #eeeeee;
    font-family: 'Montserrat', sans-serif;
    display: grid;
    grid-template-rows: auto;
    justify-items: center;
    align-items: center;
  }

  body, html {
    margin: 0;
    height: 100%;
  }

  #app {
    width: 50%;
  }
</style>
