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
          <div class="base_controls_content d-flex flex-column justify-space-around align-center">

            <div class="base_controls_form">
              <div class="base_controls_label">
              E-mail:
            </div>

            <input 
              class="base_controls_input"
              v-model="email"
              >

              <div class="base_controls_label">
              Password:
            </div>

            <input 
              class="base_controls_input"
              type="password"
              v-model="password"
              >
            </div>
            <div class="base_controls_label" v-if="loginError" style="color:red;">
              User with given credentials does not exist 
            </div>
            
          
            <button
              type="button"
              class="base_controls_button"
              @click="login()"
            >
              Login
            </button>
          </div>
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
  name: 'Home',

  data: () => ({

    email: '',
    password: '',
    loginError: false
      
  }),

  methods:{
    login(){
        if (this.email=='' && this.password==''){
          this.loginError = true;
        }else{
          this.loginError = false;
        }
    }

  }
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
    padding-right:20px;
  }
 .depthTxt{
  width: 10px;
    padding-left:10px;
    padding-right:20px;
  }
  .bookingTitle{
    background:#385F82;
    color:white;
    font-size: 25px;
  }
</style>

<style>
  .home{
    height: 100%;
  }
</style>

  
