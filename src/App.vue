<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/booking">Booking</router-link> |
    <router-link to="/managementHome">Management</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

#app > div{
  height: 100%;
}

nav {
  position: absolute;
  width: 100%;
  top: 5%;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
body{
  background-image: url('assets/background.jpg');
  background-position-x:  20%;
  background-size: cover;
  height: 100%;
}
html{
  height:100%;
}

.base_container{
  height: 100%;
  width: 80% !important;
  box-sizing: border-box;
  max-width: unset !important;
  padding: 0 5% !important;
}

.base_row{
  height: 100%;
}

.base_controls{
  width: 100%;
  height: 50%;
  background: rgba(255,255,255,0.75);
  padding: 2%;
}

.base_content{
  width: 100%;
  height: 75%;
  background: rgba(255,255,255,0.75);

}

.base_controls_header{
  background-color: #385F82;
  color: white;
  font-size: 24px;
  padding: 2%;
  height: 10%;
}

.base_controls_content{
  height: 90%;
  padding: 5%;
}

.base_controls_label{
  width: 100%;
  text-align: left;
  font-size: 18px;
}

.base_controls_input{
  background: white;
  border: 3px solid #085394;
  margin-bottom: 20px;
  font-size: 18px;
  width: 80%;
}

.base_controls_form{
  width: 100%;
}

.base_controls_button{
  background: #085394;
  border: 3px solid black;
  color: white !important;
  font-size: 20px;
  width: 80%;
}

.base_controls_content{
  height: 90%;
  padding: 5%;
}

.base_controls_label{
  width: 80%;
  text-align: left;
  font-size: 18px;
}

.base_controls_input{
  background: white;
  border: 3px solid #085394;
  margin-bottom: 20px;
  font-size: 18px;
  width: 80%;
  padding: 2px;
}

.base_controls_form{
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.base_controls_button{
  background: #085394;
  border: 3px solid black;
  color: white !important;
  font-size: 20px;
  width: 80%;
}

.base_controls_error{
  width: 100%;
  text-align: center;
  color: red;
  font-size: 16px;
  margin-bottom: 20px;
  height: 20px;
}

.base_controls_dropdown{
  width: 80%;
  background: white;
  border: 3px solid #085394;
  margin-bottom: 20px;
  padding: 2px;
}

.base_controls_dropdown .v-field__input{
  padding: 0 !important;
}

</style>
