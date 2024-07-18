<template>
  <header>
    <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
        <router-link to="/" class="navbar-brand logo">
        <img src="/assets/images/logo.png" alt="logo">
<!--       <h2>Shamima Haque</h2>-->
        </router-link>
        
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse menu" id="navbarSupportedContent">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item active">
        <router-link to="/" class="nav-link" >Home</router-link>
      </li>
      <li class="nav-item">
        <router-link to="/about" class="nav-link">About</router-link>
      </li>
      <li class="nav-item">
        <router-link to="/services" class="nav-link">Services</router-link>
      </li>
       <li class="nav-item">
        <router-link to="/portfolio" class="nav-link">Portfolio</router-link>
      </li>
       <li class="nav-item">
        <router-link to="/contact" class="nav-link">Contact</router-link>
      </li>
    </ul>
  </div>
</nav>
    </div>
</header>
   
  </template>
  
  <script>
  export default{
    name: 'MyNavbar'
   }
  </script>
  <style scoped>
  </style>
  