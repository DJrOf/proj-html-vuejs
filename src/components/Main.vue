<template>
  <div>
<div class="jumbotron">
  <div class="bann">
    <div class="pick">
      <span>TODAY'S PICK</span>
    </div>
    <h1 class="corner" >Food Corner: Top Japanese Restaurants for Sushi</h1>
    <span>March, 25, 2029</span>
  </div>
</div>
  </div>
</template>

<script>
export default {
name: "Main"
}
</script>

<style>

.jumbotron {
  background-image: url("../assets/img/single-post-img3-1200x790.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 700px;
  display: flex;
  justify-content: center;
  text-align: center;
}

.bann {
  background-color: white;
  width: 30vw;
  height: 160px;
  text-align: center;
  border-radius: 18px;
  margin-top: 40vh ;
  
}

.pick {
  background-color: orange;
  border-radius: 18px;
  width: fit-content;
 text-align: center;
}

.corner {
  margin-top: 20px;
}

</style>