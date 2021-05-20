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
            <h1>Complaint Form<br>
                <span>Please fill out the following 
                form with your complaint.
                </span>
            </h1>
        </div>
        <div class="names">
            <div class="fName">
                <input type="text" v-model= "fName"
                placeholder="First Name">
                <h2>First Name</h2>
            </div>
            <div class="lName">
                <input type="text" v-model= "lName"
                placeholder="Last Name">
                <h2>Last Name</h2>
            </div>
        </div>
        <div class="email">
            <input type="email" v-model= "email"
                placeholder="Email Address">
                <h2>Email Address</h2>
        </div>
        <div class="contact">
            <input type="text" v-model= "contact"
                placeholder="Phone Number">
                <h2>Phone Number</h2>
        </div>
        <div class="reason">
            <input type="text" v-model= "reason"
                placeholder="Enter Your Reason For Complaint">
                <h2>Reason</h2>
        </div>
        <div class="complaintArea">
            <textarea v-model= "complaintArea"
                placeholder="Please Enter Your Complaint">
            </textarea>
                <h2>Complaint</h2>
        </div>
        <div class="submit">
            <router-link to="/signup"><button> Submit</button></router-link>
        </div>
    </div>
</template>

<script>

export default {
  name: 'Signup',
  data(){
    return{
      fName: '',
      lName: '',
      contact:'',
      email:'',
      complaint:'',
      reason: '',
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
        padding-top: 75px;
    }
    .back button{
        border: 2px solid #49b5e7;
       padding: 8px 15px;
       color: #49b5e7;
       font-weight: bold;
       border-radius: 10px;
       cursor: pointer;
       background: transparent;
       font-size: 17px;
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
    .title span{
        font-size: 10px;
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
    textarea{
        width: 250px;
        height: 300px;
        outline: none;
        border: none;
        font-size: 15px;
        padding: 10px;
        background: #dce4e7;
        color: #32394c;
        border-radius: 8px;
        box-shadow: 0 5px 10px 0 rgba(0, 0, 0, 0.3),
        0 7px 21px 0 rgba(0, 0, 0, 0.20);
    }
    h2{
        font-size: 12px;
        font-family: Arial, Helvetica, sans-serif;
        color: #32394c;
    }
    .names{
        display: grid;
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
}

@media only screen and (min-width: 500px){
    body{
        display: grid;
    }
    .complaint{
    margin: 2px 10px;
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
        padding: 0;
        margin: 0;
        }
    .logo{
        grid-area: l;
    }
    .back{
        grid-area: b;
        padding-top: 12px;
    }
    .back button{
        border: 2px solid #49b5e7;
        padding: 10px 25px;
        color: #49b5e7;
        font-weight: bold;
        border-radius: 10px;
        cursor: pointer;
        background: transparent;
        font-size: 18px;
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
    .title span{
        font-size: 15px;
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
    textarea{
        width: 450px;
        height: 350px;
        outline: none;
        border: none;
        font-size: 15px;
        padding: 10px;
        background: #dce4e7;
        color: #32394c;
        border-radius: 8px;
        box-shadow: 0 5px 10px 0 rgba(0, 0, 0, 0.3),
        0 7px 21px 0 rgba(0, 0, 0, 0.20);
    }
    h2{
        font-size: 12px;
        font-family: Arial, Helvetica, sans-serif;
        color: #32394c;
    }
    .names{
        display: flex;
        flex-direction: column;
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

}
   
</style>