<template>
    <div id="navBar">
      <nav >
        <router-link to="/">Home</router-link> 
        <router-link to="/user">Usuario</router-link>
        <router-link to="/admin">Admin</router-link>
      </nav>
      <router-view/>
    </div>
  </template>
  
  
  <style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: black;
  
    
    
  }
  
  nav {
    padding: 30px;
  }
  
  nav a {
    font-weight: bold;
    font-size: 30px;
    color: #2c3e50;
    margin: 15px;
  }
  nav a:hover {
    color: #ece81d;
    text-decoration: underline;
  }
  
  nav a.router-link-exact-active {
    color: #ece81d;
  }
  </style>
  