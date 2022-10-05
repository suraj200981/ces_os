<template>
  <nav>
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
  width: 100%;
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
  height: 60%;
  background: rgba(255,255,255,0.75);

}

.base_controls_header{
  background-color: #385F82;
  color: white;
  font-size: 24px;
  padding: 2%;
}
</style>
