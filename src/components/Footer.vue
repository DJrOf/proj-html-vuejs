<template>
  <footer>
    <div class="references">

      <div class="logo" >
        <img class="footlogo" src="@/assets/img/avada-food-logo-2x.png" alt="">
      </div>

      <div class="links">
          <ul v-for="item in options" :key="item" >
              <li id="space">{{item}}</li>  
          </ul>
      </div>

      <div class="contact">
        
        <ul id="foot">
          <li id="space"><h2>CONTACT</h2></li>
          <li id="space">775 New York Ave, Brooklyn, <br>
            Kings, New York 11203</li>
          <li id="space">0000-1111-3333</li>
          <li id="space">info@domain.com</li>
        </ul>
      </div>
      
      <div class="app">
      <h2>GET OUR APP!</h2>
      <ul>
        <li class="appli" ><img src="@/assets/img/download-android.png" alt=""></li>
        <li class="appli"><img src="@/assets/img/download-app-store-200x66.png" alt=""></li>
      </ul>
    </div>
    </div>

    

    <div class="copyright">
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. </p>
    </div>
      
    
  </footer>
</template>

<script>
export default {
name: "Footer",
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

footer {
  display: flex;
  flex-direction: column;
  background-color: white;
  padding: 0;
  margin: 0;
}

.references {
  display: flex;
  justify-content: center;
  margin: 0;
  padding: 3%;
}

.footlogo {
  width: 300px;
  height: 100%;
  border-right: 1px solid grey;
}

.links {
  border-right: 1px solid grey;
  text-align: center;
  width: 300px;
}

.contact {
border-right: 1px solid grey;

width: 300px;
}

.app {
width: 300px;
text-align: center;
}

#foot {
  display: flex;
  flex-direction: column;
  width: 500px;
}

.appli {
  display: block;
}

.copyright {
  height: 80px;
  background-color: aliceblue;
  color: grey;
  text-align: center;
  border-top: 1px solid grey;
  padding-top: 1%;
}



</style>