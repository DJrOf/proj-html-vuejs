<template>
  <div>

    <!-- Jumbotron -->

    <div class="jumbotron">

      <div class="bann">
        <div class="pick">
          <span>TODAY'S PICK</span>
        </div>
        <h1 class="corner" >Food Corner: Top Japanese Restaurants for Sushi</h1>
        <span>March, 25, 2029</span>
      </div>


      <!-- Foodie Journal -->

      <div class="journal">

        <div class="articles">
          <h2 class="headfoodie">FOODIE JOURNAL</h2>
          <div class="foodiecards">
            <ul v-for="inform in informs" :key="inform" >
              <li :class="inform.cardClass"> 
                <img class="picjournal" :src=" require(`../assets/img/foodiejournal/${inform.image}.jpg`)" />
              </li> 
              <li :class="inform.cardClass"> <strong>{{ inform.title }}</strong>  </li>
              <li :class="inform.cardClass"> <span>By {{ inform.author }} | {{ inform.publishedAt }} </span> </li>
            </ul>
          </div>
        </div>
      </div>

    </div>

    <!-- RECIPES -->

    <section class="recipes">

      <div class="rectext">
        <h2 class="headrec"> POPULAR RECIPES </h2>
        <p class="prec" >
          Vel eaque dolores odit dignissimos debitis magnam eos repellat sunt ut libero, culpa, <br> 
          nulla id praesentium nostrum aliquid! Provident unde molestiae officiis?
        </p>
      </div>
      
      <div class="recontent">
        <div class="recarticle">
          <div class="recimg"></div>
          <div class="artcontent">
            <h2>Lunch Favourite With Salad, Naan And Beans</h2>
            <span>Bakery, Featured, Healthy, Latest Recipes, Staff Picks</span>
            <hr>
            <p class="artext">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. 
              Quibusdam laborum, ut tempora temporibus, unde quod cumque sapiente atque, 
              quae commodi iure in qui tenetur quos! Illo ipsam modi debitis amet?
              Lorem ipsum dolor sit amet consectetur adipisicing elit. 
              Quibusdam laborum, ut tempora temporibus, unde quod cumque sapiente atque, 
              quae commodi iure in qui tenetur quos! Illo ipsam modi debitis amet?
            </p>
            <button class="reclearn">LEARN MORE</button>
          </div>
        </div>
        <div class="recpics">
          <ul v-for="item in populaRecipes" :key="item" >
            <li> 
              <img class="picrec" :src=" require(`../assets/img/recipes/${item}.jpg`)" />
            </li>
          </ul> 
        </div>
      </div>

    <!-- CULINARY COLLECTION -->

      <div class="rectext">
        <h2 class="headrec"> CULINARY COLLECTION </h2>
        <p class="prec" >
          Vel eaque dolores odit dignissimos debitis magnam eos repellat sunt ut libero, culpa, <br> 
          nulla id praesentium nostrum aliquid! Provident unde molestiae officiis?
        </p>
      </div>

      <div class="piclist">
          <ul class="picard" v-for="culinaryCollection in culinaryCollections" :key="culinaryCollection" >
            <li> 
              <img class="picul" :src=" require(`../assets/img/collection/${culinaryCollection.pic}.png`)" />
            </li>
            <li>{{ culinaryCollection.name }}</li>
          </ul> 
      </div>
    </section>


    <!-- FARM TO TABLE -->

    <section class="farmtotable">

      <div class="farmtext">
        <div>
          <h2 class="headfarm"> FARM TO TABLE </h2>
          <p class="pfarm" >
            Vel eaque dolores odit dignissimos debitis magnam eos repellat sunt ut libero, culpa, <br> 
            nulla id praesentium nostrum aliquid! Provident unde molestiae officiis?
          </p>
        </div>
        <button class="btnblog" >READ OUR BLOG</button>
      </div>


      <div class="fttcont">

        <div class="left">
          <div class="fttarticle">
            <div class="fttimg"></div>
            <div class="ftcontent">
              <h2>Lunch Favourite With Salad, Naan And Beans</h2>
              <span>Bakery, Featured, Healthy, Latest Recipes, Staff Picks</span>
              <hr>
              <p class="fttext">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Quibusdam laborum, ut tempora temporibus, unde quod cumque sapiente atque, 
                quae commodi iure in qui tenetur quos! Illo ipsam modi debitis amet?
                  
              </p>
              <div class="little">
                <span>Read More ></span>
              </div>
            </div>
          </div>

          <div class="blogcards">
            
            <ul class="blogcard" v-for="blog in blogs" :key="blog" >
              <li > 
                <img class="picblog" :src=" require(`../assets/img/blog/${blog.image}.jpg`)" />
              </li> 
              <li class="blogli" > <strong>{{ blog.title }}</strong>  </li>
              <li class="blogli"> <span>By {{ blog.author }} | {{ blog.publishedAt }} </span> </li>
            </ul>
         
            <button class="btnmoreblog" >LOAD MORE POSTS</button>

          </div>

        </div>

        <div class="right">

          <div class="latest">
            <h2 class="lastrechead">VIEW OUR LAST RECIPES</h2>
          </div>

          <div class="singapore">
            <h2 class="guide">City Guide: Singapore</h2>
            <button class="guidebtn">VIEW ALL CITY GUIDES</button>
          </div>
          <hr>
          <input class="searchright" type="text" placeholder="Search...">
          <div class="social">
            <h3 class="follow" >Follow Us</h3>
            <ul class="rightsocial" >
              <li class="lisocial" >FB</li>
              <li class="lisocial" >IG</li>
              <li class="lisocial" >Tw</li>
              <li class="lisocial" >YT</li>
            </ul>
          </div>

          <div class="btnpoprec">
            <div class="pop">
              <h3>Popular</h3>
            </div>
            <div class="recen">
              <h3>Recent</h3>
            </div>
          </div>

          <div class="poplist">
            <ul class="popbann" v-for="popularArticle in popularArticles" :key="popularArticle" >
              <li class="popli" > 
                <img class="picpop" :src=" require(`@/assets/img/popular/${popularArticle.image}.jpg`)" />
              </li>
              <li class="popli">{{ popularArticle.title }} <br>
              <span>{{ popularArticle.publishedAt }}</span></li>
            </ul> 
          </div>

           <div class="tweets">
            <h2 class="by" > <img class="profpic" src="@/assets/img/videographer-1-400x300.jpg"> Tweets by <a href="">@Theme_Fusion</a></h2>
            <span>@Theme_Fusion</span>
            <p class="tweetcontent" >Lorem ipsum dolor sit amet consectetur adipisicing elit. 
              Voluptatibus numquam, vero aliquid deserunt hic nisi est iure aspernatur architecto consequatur reprehenderit. 
              In impedit omnis corporis error adipisci possimus quis veniam. <br>
              <a href="#">https://fakelink.org</a> </p>
              <img class="tweetpic" src="@/assets/img/videographer-1-400x300.jpg" alt="">
          </div>

        </div>
      </div>
    </section>

    <section class="subscribe">
      <div class="textsub">
        <h2>Subscribe &#38; Receive A Free eBook</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. 
          Voluptatibus minus ea consectetur eum repellendus quia nam cum dolore ipsa dignissimos eos.</p>
          <div class="formail">
            <input class="searchsub" type="text">
            <button class="subtn" >SUBSCRIBE</button>
          </div>
          <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</span>
      </div>
    </section>

    <section class="reel">
      <div class="reelpics">
        <ul  class="reelcard" v-for="item in reels" :key="item" >
            <li class="showreel" > 
              <img class="reelimg" :src=" require(`../assets/img/reel/${item}.jpg`)" />
            </li>
          </ul> 
      </div>
    </section>

  </div>
</template>

<script>
export default {
name: "Main",
data: () => {
  return {
    informs: [
        { title: 'Food Corner: Top Japanese Restaurants for Sushi', image: 1, author: 'admin1', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal'},
        { title: 'Roundup: My New Favourite recepies For Healthy Living',image: 2, author: 'admin2', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' },
        { title: 'Why These Toasts with Tea are My New Favourite', image: 3, author: 'admin3', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' }
      ],
      populaRecipes: [
        1, 2, 3, 4, 5, 6, 7, 8
      ],
      culinaryCollections: [
        { name: 'DRINKS', pic: 1},
        { name: 'SOUPS',pic: 2},
        { name: 'BAKERY', pic: 3},
        { name: 'DINNER', pic: 4},
        { name: 'HEALTHY',pic: 5},
        { name: 'STAFF PICKS', pic: 6},
        { name: 'APPETISERS', pic: 7},
        { name: 'QUICK & EASY',pic: 8}
      ],
      blogs: [
        { title: '5 Waterside Restaurants in Istambul for Special Events', image: 1, author: 'admin1', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal'},
        { title: 'Roundup: My New Favourite recepies For Healthy Living',image: 2, author: 'admin2', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' },
        { title: 'Why These Toasts with Tea are My New Favourite', image: 3, author: 'admin3', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' },
        { title: 'Meal Prep: Korean BIBIMbap with Kimchi', image: 4, author: 'admin1', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal'},
        { title: 'Exploring Street Food in Bangkok' ,image: 5, author: 'admin2', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' },
        { title: 'Organic Choices For healthier Living', image: 6, author: 'admin3', publishedAt: 'march 25th, 2019', cardClass: 'foodiejournal' }
      ],
      popularArticles: [
        { title: 'Food Corner: Top Japanese Restaurants for Sushi', image: 1, publishedAt: 'march 25th, 2019'},
        { title: 'Roundup: My New Favourite recepies For Healthy Living',image: 2, publishedAt: 'march 25th, 2019' },
        { title: 'Why These Toasts with Tea are My New Favourite', image: 3, publishedAt: 'march 25th, 2019' }
      ],
      reels: [
        1, 2, 3, 4
      ],
    };
  }
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
  flex-direction: column;
}

.bann {
  background-color: white;
  width: 30vw;
  height: 160px;
  text-align: center;
  border-radius: 18px;
  margin-top: 70px;
  margin-left: 35%;
  position: absolute;
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

.journal {
  display: flex;
  justify-content: center;
  margin: 0;
}

.headfoodie {
  display: block;
  text-align: center;
}

span {
  color: grey;
}

.articles {
  width: 1000px;
  height: auto;
  display: flex;
flex-direction: column;
justify-content: center;
background-color: white;
margin-top: 900px;
padding: 2%;
}

.foodiecards {
display: flex;
}

.foodiejournal {
display: flex;
justify-content: center;
margin-top: 10px;
}

ul {
padding: 0;
}

.picjournal {
  width: 300px;
}

.recipes {
  margin-top: 400px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: aliceblue;
}

.rectext {
  text-align: center;
  color: grey;
  margin-bottom: 60px;
}

.recontent {
  display: flex;
  justify-content: space-around;
  margin-bottom: 100px;
}

.recarticle {
  height: 750px;
  width: 500px;
  background-color: white;
}

.recpics {
  height: 750px;
  width: 500px;
  
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.recimg {
  height: 300px;
  background-image: url('~@/assets/img/Yogurt-Nan-600x395.jpg');
  background-repeat: no-repeat;
  background-position: contain;
}

.artcontent {
padding: 3%;
background-color: white;
}

.artext {
  line-height: 30px;
}

.reclearn {
  padding: 1%;
  color: white;
  background-color: orange;
  border: none;
  height: 40px;
  width: 130px;
}

.picrec {
  width: 200px;
}

.piclist {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.picard {
  width: calc((100vw / 12) * 3 - 40px);
  height: 200px;
  background-color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}

.picul {
  width: 100px;
}

.farmtotable {
  padding: 2%;
  height: 2200px;
}

.farmtext {
  display: flex;
  justify-content: space-between;
  margin-bottom: 40px;
}

.btnblog {
  color: white;
  background-color: orange;
  border: none;
  width: 180px;
  height: 40px;
  margin-top: 40px;
}

.fttcont {
  display: flex;
  justify-content: space-around;
}

.left {
  width: calc((100vw / 12) * 8 - 400px );
  height: 1400px;
  background-color: aliceblue;
}

.blogcards {
  display: flex;
  margin: 0;
 flex-wrap: wrap;
 width: calc((100vw / 12) * 8 - 400px );
 text-align: center;
 justify-content: space-around;
 
}

.blogcard {
  width: 275px;
  display: flex;
  flex-direction: column;
  
  background-color: white;
  line-height: 20px;
  padding-bottom: 30px;
  height: 300px;
  text-align: center;
}

.fttimg {
  height: 300px;
  background-image: url('~@/assets/img/single-post-img3-600x395.jpg');
  background-repeat: no-repeat;
  background-position: cover; 
}

.ftcontent {
  padding: 3%;
  background-color: white;
}

.right {
  width: calc((100vw / 12) * 4 - 100px );
  height: 800px;
}

.picblog {
  width: 275px;
  margin: 0;
}

.blogli {
  margin-top: 20px;
}

.btnmoreblog {
  width: 100%;
  border: none;
  color: white;
  height: 30px;
  background-color: grey;
}

.latest {
  width: calc((100vw / 12) * 4 - 50px );
  height: 500px;
  background-image: url('~@/assets/img/ad-bg.jpg');
  background-repeat: no-repeat;
  background-size: contain; 
}

.lastrechead {
position: absolute;
margin-top: 200px;
margin-left: 135px;
width: 150px;
}

.singapore {
width: calc((100vw / 12) * 4 - 100px );
  height: 340px;
  background-image: url('~@/assets/img/singapore-featured-image-600x395.jpg');
  background-repeat: no-repeat;
  background-size: contain; 
  margin-top: 30px;
}

.guide {
background-color: black;
color: white;
margin-top: 170px;
position: absolute;
}

.guidebtn {
color: white;
  background-color: orange;
  border: none;
  width: 100%;
  height: 40px;
  margin-top: 250px;
}

.searchright {
  width: 98%;
  height: 40px;
  margin-top: 30px;
}

.rightsocial {
  list-style: none;
}

.lisocial {
  display: inline;
  margin-left: 10px;
}

.follow {
  color: orange;
}

.btnpoprec {
  display: flex;
  margin-top: 60px;
  margin-bottom: 40px;
}

.pop {
  width: 50%;
  background-color: white;
  color: black;
  border: 1px solid grey;
  text-align: center;
}

.recen {
  width: 50%;
  background-color: aliceblue;
  color: black;
  border: 1px solid grey;
  text-align: center;
}

.picpop {
  width: 50px;
  border-radius: 50%;
  float: left;
  margin-right: 20px;
}

.popli {
display: block
}

.tweets {
width: calc((100vw / 12) * 4 - 100px );
height: 500px;
background-color: white;
margin-top: 50px;
text-align: left;
padding: 5%;
}

.tweetcontent {
  color: black;
}

.tweetpic {
  width: 350px;
  height: 200px;
}

.profpic {
  width: 50px;
  height: 50px;
  border-radius: 50%; 
}

.subscribe {
  background-image: url('~@/assets/img/subscribe-sec-bg.png');
  background-repeat: no-repeat;
  background-size: contain; 
  height: 500px;
 display: flex;
 justify-content: center;
}

.textsub {
 text-align: center;
 padding-top: 100px;
 width: 600px;
}

.searchsub {
  width: 60%;
  height: 40px;
  margin-top: 30px;
}

.subtn {
  color: white;
  background-color: orange;
  border: none;
  width: 20%;
  height: 40px;
  margin-left: 2%;
}

.formail {
  margin-bottom: 20px;
}

.reelpics {
height: 500px;
 display: flex;
 
}

.showreel {
display: inline;

}

.reelcard {
width: calc((100vw / 12) * 4 - 140px);
}

.reelimg {
width: calc((100vw / 12) * 4 - 140px);
}

</style>