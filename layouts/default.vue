<template>


  
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/product">Product</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/limitmessage">Limit Message </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/previewImage">PreviewImage</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<slot />



<div class="page-container fixed-bottom">
<footer class="bg-dark text-center text-white">
    <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2);font-size: 25px;">
   <a href="https://www.facebook.com/alongkon29/" target="_blank" class="m-3">   <i class="bi bi-facebook"></i></a>
  <a href="http://www.106planet.com/66309010021/" target="_blank">  <i class="bi bi-globe-americas"></i></a>
     
    </div>
    <div class="text-center p-3 " style="background-color: rgba(0, 0, 0, 0.2);">
      © 2020 Copyright:
      <a class="text-white" href="#">alongkon</a>
    </div>
   
    <!-- Copyright -->
  </footer>
</div>
</template>

<style>
a {
  text-decoration: none;
  color: white;
}

section {
  justify-content: center;
  flex-direction: column;
}

</style>

