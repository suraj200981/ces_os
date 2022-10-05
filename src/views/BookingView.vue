<template>
    <div>
      <Booking/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import Booking from '@/components/Booking.vue'
  
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'BookingView',
    components: {
        Booking
    }
  }
  </script>
  