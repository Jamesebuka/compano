<template>
  <div class="complaint">
        <div class="nav">
            <div class="logo">
                <router-link to="/"> <h3>Complano</h3></router-link>
              </div>
            <div class="back">
                <router-link to="/"><button> Back</button></router-link>
            </div>
        </div>
        <div class="title">
            <h1>Login</h1>
        </div>
        <div class="email">
            <input type="email" v-model= "email"
                placeholder="Email Address">
                <h2>Email Address</h2>
        </div>
        <div class="contact">
            <input type="password" v-model= "contact"
                placeholder="Password">
                <h2>Password</h2>
        </div>
        <div class="submit">
            <router-link to="/signup"><button> Submit</button></router-link>
        </div>
    </div>
</template>

<script>

export default {
  name: 'Login',
  data(){
    return{
      email: '',
      password: ''
    }
  }
}
</script>

<style scoped>
@media only screen and (min-width: 100px) and (max-width: 500px){
    body{
        display: grid;
    }
    .complaint{
    margin: 5px 5px;
    width: 100%;
    height: auto;
    display: grid;
    text-align: center;
    }
    .logo a{
        background: white;
        color: #32394c;
        font-weight: bold;
        font-family: cursive;
        padding-top: 1px;
        font-size: 25px; 
      }
    .logo{
        grid-area: l;
    }
    .back{
        grid-area: b;
        padding-top: 69px;
    }
    .back button{
        border: 2px solid #49b5e7;
       padding: 10px 25px;
       color: #49b5e7;
       font-weight: bold;
       border-radius: 10px;
       cursor: pointer;
       background: transparent;
       font-size: 12px;
       font-family: cursive;
     }
     .back button:hover{
       color: white;
       background: #49b5e7;
     }
    .nav{
        display: grid;
        grid-template-areas:
        "l . b";
    }
    .title h1{
        font-size: 18px;
        font-family: cursive;
        color: #32394c;
    }
    .title{
        display: flex;
        flex-direction: column;
    }
    input{
        background: transparent;
        max-width: 300px;
        padding: 8px 15px;
        border: 1px solid #32394c;
        border-radius: 8px;
        color: #32394c;
    }
    input:focus{
        outline: none;
        border: 1px solid #32394c;
    }
    h2{
        font-size: 12px;
        font-family: Arial, Helvetica, sans-serif;
        color: #32394c;
    }
    .submit button{
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
     .submit button:hover{
       color: white;
       background: #49b5e7;
     }
     .contact{
         padding-top: 30px;
     }
     .email{
         padding-top: 30px;
     }
     .submit{
         padding-top: 30px;
     }
}

@media only screen and (min-width: 500px){
    body{
        display: grid;
    }
    .complaint{
    margin: 10px 10px;
    width: 100%;
    height: auto;
    display: grid;
    text-align: center;
    }
    .logo a{
        background: white;
        color: #32394c;
        font-weight: bold;
        font-family: cursive;
        font-size: 25px; 
        }
    .logo{
      padding: 0;
      margin: 0;
        grid-area: l;
    }
    .back{
        grid-area: b;
        padding-top: 65px;
    }
    .back button{
        border: 2px solid #49b5e7;
        padding: 10px 25px;
        color: #49b5e7;
        font-weight: bold;
        border-radius: 10px;
        cursor: pointer;
        background: transparent;
        font-size: 13px;
        font-family: cursive;
        }
    .back button:hover{
        color: white;
        background: #49b5e7;
        }
    .nav{
        display: grid;
        grid-template-areas:
        "l . b";
    }
    .title h1{
        font-size: 35px;
        font-family: cursive;
        color: #32394c;
    }
    .title{
        display: flex;
        flex-direction: column;
    }
    input{
        background: transparent;
        width: 500px;
        padding: 8px 15px;
        border: 1px solid #32394c;
        border-radius: 8px;
        color: #32394c;
    }
    input:focus{
        outline: none;
        border: 1px solid #32394c;
    }
    h2{
        font-size: 12px;
        font-family: Arial, Helvetica, sans-serif;
        color: #32394c;
    }
  
    .submit button{
        border: 2px solid #49b5e7;
        padding: 10px 25px;
        color: #49b5e7;
        font-weight: bold;
        border-radius: 10px;
        cursor: pointer;
        background: transparent;
        font-size: 17px;
        font-family: cursive;
        width: 300px;
        }
        .submit button:hover{
        color: white;
        background: #49b5e7;
        }

}
   
   
</style>