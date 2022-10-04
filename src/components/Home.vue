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
        >
          <h3>Login</h3>
          <v-card-text>Email:</v-card-text>
          <v-text-field
            label="Email"
            solo
          ></v-text-field>
          <v-card-text>Password:</v-card-text>
          <v-text-field
            label="Password"
            solo
          ></v-text-field>
          <v-btn
  elevation="2"
  large
>Login</v-btn>
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
  name: 'Home',

  data: () => ({
   
  }),
}
</script>
