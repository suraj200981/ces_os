<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3" style="color:white;">
          Welcome to Oceanic Airlines
        </h1>
      
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
       
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
      <v-row no-gutters>
      <v-col>
        <v-card
          class="pa-2"
          outlined
          elevation="2"
          tile
          style="background-color: rgba(255, 255, 255, .6);"
          width="350px"
        >
          <h3 class="bookingTitle">Login</h3>
          <v-card-text style="text-align:left !important;"><b>Email:</b></v-card-text>
          <v-text-field
            v-model="message4"
            label="Email address"
            outlined
            clearable
          ></v-text-field>
      <v-card-text style="text-align:left !important;"><b>Password:</b></v-card-text>
      <v-text-field
            v-model="message4"
            label="Password"
            outlined
            clearable
          ></v-text-field>

          <v-btn
  elevation="2"
  large
  style="background:#315473; color: white;"
>Search</v-btn>
        </v-card>
      </v-col>
      <v-col order="12">
        <v-card
        class="cardColor"
          outlined
          tile
        >
          
        </v-card>
      </v-col>
      <v-col order="1">
        <v-card
        class="cardColor"
          outlined
          tile
        >
          
        </v-card>
      </v-col>
    </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
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
/deep/ .widthTxt{
    width: 10px;
    padding-left:10px;
    padding-right:20px;
}
/deep/ .heightTxt{
  width: 10px;
    padding-left:10px;
    padding-right:20px;}
/deep/ .depthTxt{
  width: 10px;
    padding-left:10px;
    padding-right:20px;}
    .bookingTitle{
      background:#385F82;
      color:white;
      font-size: 25px;
    }
</style>
