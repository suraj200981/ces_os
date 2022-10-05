<template>
  <v-container class="base_container">
    <v-row class="base_row">
      <v-col 
        cols="3"
        class="d-flex align-center"
      >
        <div class="base_controls">
          <div class="base_controls_header">
              Login
          </div>
          <v-row>
            <v-card-text style="text-align:left !important;"
            >
              <b>Email:</b>
            </v-card-text>

            <v-text-field
              v-model="message4"
              label="Email address"
              outlined
              clearable
            ></v-text-field>

            <v-card-text 
              style="text-align:left !important;"
            >
              <b>Password:</b>
            </v-card-text>

            <v-text-field
              v-model="message4"
              label="Password"
              outlined
              clearable
            >
            </v-text-field>

            <v-btn
              elevation="2"
              large
              style="background:#315473; color: white;"
            >
              Login
            </v-btn>
          </v-row>
        </div>
      </v-col>

      <v-col
        cols="9"
        class="d-flex align-center"
      >
      <div class="base_content"></div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Booking',

  data: () => ({
      
  }),
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
  .home{
  height: 100%;
  }
</style>

  
