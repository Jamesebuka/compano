<template>
  <div class="home">
    
    <div class="header">
      <!--Logo component-->
      <div class="logo">
        <router-link to="/"> <h3>Complano</h3></router-link>
      </div>

      <!-- Nav links component -->
        <div class="nav">
            <router-link to="/">Home</router-link> 
            <router-link to="/services">Services</router-link> 
            <router-link to="/login">Login</router-link> 
            <router-link to="/about">About us</router-link> 
            <router-link to="/contact">Contact</router-link>
        </div> 

      <!-- signup link  -->
        <div class="signup">
          <div class="menu">
            <h3 @click= "toggle" v-show= "!show">Menu</h3>
          </div>
          <router-link to="/signup"><button> sign up </button></router-link>   
        </div>
        <!-- signup link end -->

    </div>

    <div class="main">
      <div class="pageImage">
        <img alt="Vue logo" src="@/assets/hero.png">
      </div>
      <div class="writeUp">
        <h2>Complano.org </h2>
        <h3> Is an organization established to help both up coming businesses and
          old businesses get fact from their respective customer.
        </h3>
        <h2>Objectives </h2>
        <h3>We help businesses get feed back from their customers.</h3>
        <h3>We ensure customer's feedback is sent to the appropriate organization.</h3>
          
      </div>
        <div v-show= "show" class="menu-nav">
            <h1 @click= "toggle">x</h1>
            <router-link to="/">Home</router-link> 
            <router-link to="/services">Services</router-link> 
            <router-link to="/login">Login</router-link> 
            <router-link to="/about">About us</router-link> 
            <router-link to="/contact">Contact</router-link>  
            <router-link to="/signup"><button> sign up </button></router-link>          
            

        </div>
        
    </div>

    <div class="footer">              
      <div class="copyRight">
          <div class="copy">Copyright &copy; 2021, all rights reserved</div>
          <div class="socialMedia">
          
            <a href="#">
                <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg">
                    <path d="M6.023 16L6 9H3V6h3V4c0-2.7 1.672-4 4.08-4 1.153 0 2.144.086 2.433.124v2.821h-1.67c-1.31 0-1.563.623-1.563 1.536V6H13l-1 3H9.28v7H6.023z" fill="#0270D7"/>
                </svg>
            </a>
          
            <a href="#">
                <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.9 7v2.4H12c-.2 1-1.2 3-4 3-2.4 0-4.3-2-4.3-4.4 0-2.4 2-4.4 4.3-4.4 1.4 0 2.3.6 2.8 1.1l1.9-1.8C11.5 1.7 9.9 1 8 1 4.1 1 1 4.1 1 8s3.1 7 7 7c4 0 6.7-2.8 6.7-6.8 0-.5 0-.8-.1-1.2H7.9z" fill="#0270D7"/>
                </svg>
            </a>
        
            <a href="#">
                <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 3c-.6.3-1.2.4-1.9.5.7-.4 1.2-1 1.4-1.8-.6.4-1.3.6-2.1.8-.6-.6-1.5-1-2.4-1-1.7 0-3.2 1.5-3.2 3.3 0 .3 0 .5.1.7-2.7-.1-5.2-1.4-6.8-3.4-.3.5-.4 1-.4 1.7 0 1.1.6 2.1 1.5 2.7-.5 0-1-.2-1.5-.4C.7 7.7 1.8 9 3.3 9.3c-.3.1-.6.1-.9.1-.2 0-.4 0-.6-.1.4 1.3 1.6 2.3 3.1 2.3-1.1.9-2.5 1.4-4.1 1.4H0c1.5.9 3.2 1.5 5 1.5 6 0 9.3-5 9.3-9.3v-.4C15 4.3 15.6 3.7 16 3z" fill="#0270D7"/>
                </svg>
            </a>
      
        </div>
      </div>
      </div>

  </div>
     
  
</template>

<script>

export default {
  name: 'Home',
  data(){
    return{
      show: false
    }
  },
  methods: {
    toggle: function() {
      this.show = !this.show;
    }
  }
}
</script>

<style scoped>
.home{
  display: grid;
  margin: 20px 40px;
  grid-template-rows: 20vh 48vh 20vh;
}
.logo a{
  grid-area: l;
  background: white;
  color: #32394c;
  font-weight: bold;
  font-family: cursive;
  padding-top: 1px;
  font-size: 30px; 
}
.nav{
  background: rgb(255, 255, 255);
  padding-top: 51px;
  grid-area: n;
}
.signup{
  /* background: white; */
  font-family: cursive;
  padding-top: 35px;
  font-size: 17px; 
  color: #32394c;
  grid-area: s;
}
.signup button{
   border: 2px solid #49b5e7;
  padding: 10px 25px;
  color: #49b5e7;
  font-weight: bold;
  border-radius: 10px;
  cursor: pointer;
  background: transparent;
  font-size: 17px;
  font-family: cursive;
}
.signup button:hover{
  color: white;
  background: #49b5e7;
}
.header{
  display: grid;
  grid-template-areas:
  "l n n s";
}
.pageImage{
  grid-area: p;
}
.pageImage img{
  width: 550px;
  height: auto;
}
.writeUp{
  padding-top: 65px;
  grid-area: w;
}
.writeUp h3{
  font-family: 'Courier New', Courier, monospace;
}
.writeUp h4{
  font-family: cursive; 
  font-size: 16px;
}
span{
  font-family: cursive;
  color: #32394c;
  font-weight: bold;
  font-size: 20px;

}
.writeUp button{
  border: 2px solid #49b5e7;
  padding: 15px 25px;
  color: #49b5e7;
  font-weight: bold;
  border-radius: 10px;
  cursor: pointer;
  background: transparent;
  font-size: 17px;
  font-family: cursive;
}
.writeUp button:hover{
  color: white;
  background: #49b5e7;
  border: none;
}
.main{
  display: grid;
  grid-template-areas:
  "p w";
}
.copy{
  grid-area: c;
}
.socialMedia{
  grid-area: sm;
  display: flex;
  justify-content: center;
  justify-content: space-around;
}
.copyRight{
  padding-top: 100px;
  grid-area: cr;
  display: grid;
  grid-template-areas:
  ". . . . ."
  ". . . . ."
  "c . . . sm"
  ". . . . ." ;
}
.copyRight{
  color: rgb(95, 92, 92);
}
 .menu{
    display: none;
  }
  .menu-nav{ 
    width: 70%;
    position: absolute;
    display: none;
    background: #d3e3f5;
    padding-top: 51px;
    grid-area: mn;
  }
  .menu-nav button{
  border: 2px solid #49b5e7;
  padding: 8px 10px;
  color: #49b5e7;
  font-weight: bold;
  border-radius: 10px;
  cursor: pointer;
  background: white;
  font-size: 20px;
  font-family: cursive;
}
.menu-nav button:hover{
  color: white;
  background: #49b5e7;
}
@media only screen and (min-width: 890px) and (max-width: 1030px){
  .home{
  display: grid;
  margin: 5px 30px;
  grid-template-rows: 10vh 80vh 20vh;
  }
  .pageImage img{
  width: 400px;
  height: auto;
  padding-top: 90px;
  }
  .writeUp{
  padding-top: 15px;
  grid-area: w;
  }
  .header{
  display: grid;
  grid-template-areas:
  "l . . s";
}
.nav{
  display: none;
}
.signup button{
  display: none;
}
  .menu{
    display: block;
    right: 5px;
    cursor: pointer;
    text-shadow: 1px 2px 4px #32394c;
  }
  .menu:hover{
    color: #49b5e7;
    font-size: 18px;
  }
  .main{
  display: grid;
  grid-template-areas:
  "p mn"
  "w mn";
  }
  .menu-nav{
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    border-radius: 9px;
  }
  .menu-nav h1{
    text-align: center;
    font-size: 25px;
    color: #32394c;
    cursor: pointer;
  }
  .menu-nav h1:hover{
    font-size: 26px;
  }
  .copyRight{
    padding-top: 100px;
  }
}
@media only screen and (min-width: 673px) and (max-width: 890px){
  .home{
  display: grid;
  margin: 5px 30px;
  grid-template-rows: 10vh 80vh 20vh;
  }
  .logo a{
  font-size: 30px; 
}
  .pageImage img{
  width: 300px;
  height: auto;
  padding-top: 90px;
  }
  .writeUp{
  padding-top: 15px;
  grid-area: w;
  }
  .header{
  display: grid;
  grid-template-areas:
  "l . . s";
}
.nav{
  display: none;
}
.signup button{
  display: none;
}
  .menu{
    display: block;
    right: 5px;
    cursor: pointer;
    text-shadow: 1px 2px 4px #32394c;
  }
  .menu:hover{
    color: #49b5e7;
    font-size: 18px;
  }
  .main{
  display: grid;
  padding-top: 20px;
  grid-template-areas:
  "mn mn"
  "p p"
  "w w";
  }
  .menu-nav{
    display: flex;
    flex-direction: column;
    border-radius: 10px;
  }
  .menu-nav h1{
    text-align: center;
    font-size: 25px;
    color: #32394c;
    cursor: pointer;
  }
  .menu-nav h1:hover{
    font-size: 26px;
  }
  .copyRight{
    padding-top: 90px;
  }
.copyRight{
  color: rgb(95, 92, 92);
  /* padding-top: 450px; */
}
}

@media only screen and (min-width: 357px) and (max-width: 673px){
  .home{
  display: grid;
  margin: 5px 30px;
  grid-template-rows: 10vh 80vh 20vh;
  }
  .logo a{
  font-size: 30px; 
}
  .pageImage img{
  width: 250px;
  height: auto;
  padding-top: 90px;
  }
  .writeUp{
  padding-top: 15px;
  grid-area: w;
  }
  .header{
  display: grid;
  grid-template-areas:
  "l . . s";
}
.nav{
  display: none;
}
.signup button{
  display: none;
}
  .menu{
    display: block;
    right: 5px;
    cursor: pointer;
    text-shadow: 1px 2px 4px #32394c;
  }
  .menu:hover{
    color: #49b5e7;
    font-size: 18px;
  }
  .main{
  display: grid;
  padding-top: 20px;
  grid-template-areas:
  "mn mn"
  "p p"
  "w w";
  }
  .menu-nav{
    display: flex;
    flex-direction: column;
    border-radius: 10px;
  }
  .menu-nav h1{
    text-align: center;
    font-size: 25px;
    color: #32394c;
    cursor: pointer;
  }
  .menu-nav h1:hover{
    font-size: 26px;
  }
  .copyRight{
    padding-top: 90px;
  }
.copyRight{
  padding-top: 90px;
}
.copyRight{
grid-area: cr;
display: grid;
grid-template-areas:
". sm sm ."
". . . . "
". . .  ."
". c c . " ;
}
.socialMedia{
  padding-top: 35px;
}
.copyRight{
  color: rgb(95, 92, 92);
  padding-top: 25px;
}

@media only screen and (min-width: 50px) and (max-width: 357px){
  .home{
  display: grid;
  margin: 5px 20px;
  grid-template-rows: 10vh 80vh 20vh;
  }
  .logo a{
  font-size: 20px; 
}
  .pageImage img{
  width: 100px;
  height: auto;
  padding-top: 90px;
  }
  .writeUp{
  padding-top: 15px;
  grid-area: w;
  }
  .header{
  display: grid;
  grid-template-areas:
  "l . . s";
}
.nav{
  display: none;
}
.signup button{
  display: none;
}
  .menu{
    display: block;
    right: 5px;
    cursor: pointer;
    text-shadow: 1px 2px 4px #32394c;
  }
  .menu:hover{
    color: #49b5e7;
    font-size: 18px;
  }
  .main{
  display: grid;
  padding-top: 20px;
  grid-template-areas:
  "mn mn"
  "p p"
  "w w";
  }
  .menu-nav{
    display: flex;
    flex-direction: column;
    border-radius: 10px;
  }
  .menu-nav h1{
    font-size: 25px;
    color: #32394c;
    cursor: pointer;
  }
  .menu-nav h1:hover{
    font-size: 26px;
  }
  .copyRight{
    padding-top: 90px;
  }
.copyRight{
  padding-top: 90px;
}
.copyRight{
grid-area: cr;
display: grid;
grid-template-areas:
". sm sm ."
". . . . "
". . .  ."
". c c . " ;
}
.socialMedia{
  padding-top: 35px;
}
.copyRight{
  color: rgb(95, 92, 92);
  padding-top: 25px;
}
}

}

</style>