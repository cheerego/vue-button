<template>
  <div>
    <BaseButton>Base</BaseButton>
    <TypeButton @click="defaul" type="defaul">defaul</TypeButton>
    <TypeButton @click="primary" type="primary">primary</TypeButton>
    <TypeButton @click="info" type="info">info</TypeButton>
    <TypeButton @click="success" type="success">success</TypeButton>
    <TypeButton @click="warning" type="warning">warning</TypeButton>
    <TypeButton @click="danger" type="danger">danger</TypeButton>
  </div>
</template>

<script>
  import TypeButton from './components/TypeButton.vue'
  import BaseButton from './components/BaseButton.vue'
  export default {
    data() {
      return {}
    },
    methods: {
      defaul(){
        console.log('defaul')
      },
      primary(){
        console.log('primary')
      },
      info(){
        console.log('info')
      },
      success(){
        console.log('success')
      },
      warning(){
        console.log('warning')
      },
      danger(){
        console.log('danger')
      },
    },
    components: {
      TypeButton,
      BaseButton
    }
  }
</script>

<style>
</style>
