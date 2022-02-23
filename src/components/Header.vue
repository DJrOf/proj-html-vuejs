<template>
  <header>
      <div class="hlinks">
            <ul>
              <li id="space">Download App</li>
              <li id="space">Advertise with us</li>
          </ul>

          <ul>
              <li id="space">FB</li>
              <li id="space">IG</li>
              <li id="space">Tw</li>
              <li id="space">YT</li>
          </ul>
      </div>
      <div class="logo">
          <img src="@/assets/img/avada-food-logo.png" alt="">
      </div>
      <nav>
          
          <ul v-for="item in options" :key="item" >
              <li id="space" >{{item}}</li>  
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
name: "Header",
data: () => {
  return {
    options: [
        'Home', 'Recipes', 'Places', 'Blog', 'About', 'Contact', 'Search'
      ],
    };
  }
}
</script>

<style>

header {
    height: 160px;
}

ul {
    list-style: none;
}
#space {
    display: inline;
    margin-left: 50px;
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