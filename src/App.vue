<template>
  <v-card>
    <v-layout>
      <!-- <v-system-bar color="deep-purple darken-3"></v-system-bar> -->

      <v-app-bar
        color="primary"
        prominent
      >
        

        <v-toolbar-title>Oceanic Airlines
        </v-toolbar-title>

        <v-spacer></v-spacer>
      </v-app-bar>
    </v-layout>
  </v-card>
  <nav>
    <br>
    <br>
    <br>
    <router-link to="/">Home</router-link> |
    <router-link to="/result">Result</router-link> |
    <router-link to="/booking">Booking</router-link>
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
body{
background-image: url("C:\Users\sursh\OneDrive - Netcompany\Documents\CES\frontend 4\ces_os\src\assets\pexels-brett-sayles-1493756.jpg");
background-position-x:  20%;
background-size: cover;
}
html{
  height:100%;
}
</style>
