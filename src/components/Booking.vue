<template>
  <v-container class="base_container">
    <v-row class="base_row">
      <v-col 
        cols="3"
        class="d-flex align-center"
      >
        <div class="base_controls">
          <div class="base_controls_header">
              Booking
          </div>
          <div class="base_controls_content d-flex flex-column justify-center align-center">

            <div class="base_controls_form">
              <div class="base_controls_label">
                From:
              </div>

              <select class="base_controls_dropdown">
                <option v-for="route in routes" :key="route">{{route}}</option>
              </select>

              <div class="base_controls_label">
              To:
            </div>

            <select class="base_controls_dropdown">
              <option v-for="route in routes" :key="route">{{route}}</option>
            </select>

            <div class="base_controls_label">
              Weight (kg):
            </div>

            <input 
              class="base_controls_input"
              >

            <div class="base_controls_label">
              Size (cm):
            </div>

            <div class="size_inputs">
              <div>
                <div class="size_label">Width</div>
                <input class="size_input">
              </div>

              <div>
                <div class="size_label">Height</div>
                <input class="size_input">
              </div>

              <div>
                <div class="size_label">Depth</div>
                <input class="size_input">
              </div>
            </div>

            </div>
            
          
            <button
              type="button"
              class="base_controls_button"
            >
              Search
            </button>
          </div>
        </div>
      </v-col>

      <v-col
        cols="9"
        class="d-flex align-center"
      >
      <div class="base_content">
        <ResultComponent v-if="resultSelected == null" @resultClicked="resultSelected = $event"/>
        <ResultDetailsComponent v-if="resultSelected != null" :optimum="resultSelected == 0"/>
      </div>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
  import ResultComponent from './ResultComponent.vue';
  import ResultDetailsComponent from './ResultDetailsComponent.vue'
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Booking",
    data: () => ({
        resultSelected: null,
        row: null,
        routes: ["Congo", "Dakar", "Kabalo"],
    }),
    components: { ResultComponent, ResultDetailsComponent }
}
  </script>
  <style scoped>
   .widthTxt{
      width: 10px;
      padding-left:10px;
      padding-right:20px;
}
 .heightTxt{
    width: 10px;
      padding-left:10px;
      padding-right:20px;}
 .depthTxt{
    width: 10px;
      padding-left:10px;
      padding-right:20px;}
      .bookingTitle{
        background:#385F82;
        color:white;
        font-size: 25px;
      }

      .size_inputs{
        width: 80%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 20px;
      }

      .size_inputs > div{
        width: 30%;
      } 

      .size_input{
        width: 100%;
        background: white;
        border: 2px solid #085394;
        padding: 2px;
      }

      .size_label{
        text-align: left;
      }
  </style>
  