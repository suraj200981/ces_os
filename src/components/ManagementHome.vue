<template>
  <v-container class="base_container">
    <v-row class="base_row">
      <v-col 
        cols="3"
        class="d-flex align-center"
      >
        <div class="base_controls">
          <div class="base_controls_header">
              Management Panel
          </div>
          <div class="base_controls_content d-flex flex-column justify-start align-center">
            <div class="management_tab" :class="{management_tab_active: activePage == 0}" @click="setPage(0)">
              Users
            </div>
            <div class="management_tab" :class="{management_tab_active: activePage == 1}" @click="setPage(1)">
              Bookings
            </div>
            <div class="management_tab" :class="{management_tab_active: activePage == 2}" @click="setPage(2)">
              Route excluding
            </div>
            <div class="management_tab" :class="{management_tab_active: activePage == 3}" @click="setPage(3)">
              Statistics
            </div>
            <div class="management_tab" :class="{management_tab_active: activePage == 4}" @click="setPage(4)">
              Manage
            </div>
          </div>
        </div>
      </v-col>

      <v-col
        cols="9"
        class="d-flex align-center"
      >
      <div class="base_content" v-if="activePage != null">
        <Users v-if="activePage == 0"/>
        <ManageBookings v-if="activePage == 1"/>
        <RouteExcluding v-if="activePage == 2"/>
        <Statistics v-if="activePage == 3"/>
        <Manage v-if="activePage == 4"/>
        
      </div>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
import Users from './ManagementPages/Users.vue';
import ManageBookings from './ManagementPages/ManageBookings.vue';
import RouteExcluding from './ManagementPages/RouteExcluding.vue';
import Statistics from './ManagementPages/Statistics.vue';
import Manage from './ManagementPages/Manage.vue';
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "ManagementHome",
    data: () => ({
      activePage: null
    }),
    methods: {
      setPage: function(number){
        this.activePage = number;
      }
    },
    components: { Users, ManageBookings, RouteExcluding, Statistics, Manage }
}
  </script>
  
  <style scoped>
    .management_tab{
      color: black;
      background-color: white;
      width: 100%;
      margin-bottom: 5px;
      font-size: 20px;
      border: 3px solid black;
      cursor: pointer;
      user-select: none;
    }

    .management_tab_active{
      color: white;
      background-color: #085394;
    }
  </style>
  