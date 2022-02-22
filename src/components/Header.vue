<template>
  <header>
      <div class="hlinks">
            <ul>
              <li>Download App</li>
              <li>Advertise with us</li>
          </ul>

          <ul>
              <li>FB</li>
              <li>IG</li>
              <li>Tw</li>
              <li>YT</li>
          </ul>
      </div>
      <div class="logo">
          <img src="@/assets/img/avada-food-logo.png" alt="">
      </div>
      <nav>
          
          <ul>
              <li>Home</li>
              <li>Recipes</li>
              <li>Places</li>
              <li>Blog</li>
              <li>About</li>
              <li>Contact</li>
              <li>Searc</li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
name: "Header"
}
</script>

<style>

header {
    height: 160px;
}

ul {
    list-style: none;
}
li {
    display: inline;
}

.hlinks {
    display: flex;
    justify-content: space-around;
}

.logo {
    display: flex;
    justify-content: center;
}

nav {
    display: flex;
    justify-content: center;
}

img {
    width: 80px;
    
}




</style>