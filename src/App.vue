<template>
  <div id="app">
      <router-view/>
    
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  padding: 0;
  margin: 20px 50px;
}


#app{
  display: grid;
  background: rgb(255, 255, 255);
}
.nav a {
  font-size: 19px;
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  text-align: center;
  padding: 50px 12px;
}

.nav a.router-link-exact-active {
  color: #49b5e7;
}
.nav a:hover {
  color: #49b5e7;
}
/*  menu nav*/
.menu-nav a {
  font-size: 19px;
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  text-align: center;
  padding: 17px 12px;
}

.menu-nav a.router-link-exact-active {
  color: #49b5e7;
}
.menu-nav a:hover {
  color: #49b5e7;
}
</style>
