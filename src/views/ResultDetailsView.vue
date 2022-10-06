<template>
    <ResultDetailsComponent/>
  </template>
  
  <script>
  // @ is an alias to /src
  import ResultDetailsComponent from '@/components/ResultDetailsComponent.vue'
  
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'ResultDetailsView',
    components: {
        ResultDetailsComponent
    }
  }
  </script>
  