<template>
  <div class="signup">
    <!-- header -->
    <div class="register">
      <div class="main-header">
        <div class="logo">
          <div class="logo">
            <router-link to="/"> <h3>Complano</h3></router-link>
          </div>
        </div>
        <div class="back-btn">
          <router-link to="/"><button> Back</button></router-link>
        </div>
      </div>
      <div class="sub-header">
        <h1>Register Your Business</h1>
        <h4>Please provide all required details to register your business with us</h4>
      </div>
    </div>
    <!-- input field for business owner -->
    <div class="B-owner">
      <div class="text">
        <h1>Business Owner</h1>
      </div>
      <div class="inputs">
        <div class="inputField1">
          <input v-model= "fName">
          <h4>First Name</h4>
        </div>
        <div class="inputField2">
          <input v-model= "lName">
          <h4>Last Name</h4>
        </div>
      </div>
    </div>
    <!-- input field for business name -->
    <div class="B-name">
      <div class="text">
        <h1>Business Name</h1>
      </div>
      <div class="inputField">
        <input v-model= "fName">
      </div>
    </div>
    <!-- Contact number -->
    <div class="contact">
      <div class="text">
        <h1>Contact Number</h1>
      </div>
      <div class="inputField">
        <input v-model= "contact">
        <h4>Phone Number</h4>
      </div>
    </div>
    <!-- email -->
    <div class="email">
      <div class="text">
        <h1>Email</h1>
      </div>
      <div class="inputField">
        <input v-model= "email" placeholder="name@example.com">
      </div>
    </div>
    <!-- address -->
    <div class="address">
      <div class="text">
        <h1>Address</h1>
      </div>
      <div class="inputs">
        <div class="inputField1">
          <input v-model= "city">
          <h4>City</h4>
        </div>
        <div class="inputField2">
          <input v-model= "country">
          <h4>Country</h4>
        </div>
      </div>
    </div>
    <!-- type of business -->
    <div class="B-type">
      <div class="text">
        <h1> Type of Business</h1>
      </div>
      <div class="inputField">
        <input v-model= "typeOfBusiness">
      </div>
    </div>
    <!-- submit button -->
    <div class="submit">
      <div class="submit-btn">
          <router-link to="/signup"><button> Submit</button></router-link>
        </div>
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
      bName: '',
      contact:'',
      email:'',
      sAddress:'',
      city: '',
      country: '',
      typeOfBusiness: ''
    }
  }
}

</script>
<style scoped>
@media only screen and (min-width: 100px) and (max-width: 500px){
  .signup{
  padding: 0;
  margin: 0;
  width: 100%;
  height: auto;
  display: grid;
  justify-content: center;
  grid-template-rows: 200px 170px 90px 100px 90px 180px 90px 90px;
  }
  .register{
    display: grid;
    grid-template-areas: 
    "mh mh"
    "sh sh"
    "sh sh";
  }
  .main-header{
    grid-area: mh;
    display: grid;
    grid-template-areas: 
    "l l . bb";
  }
  .logo{
    grid-area: l;
  }
  .logo a{
    font-size: 18px;
    color: #32394c;
    font-weight: bold;
    font-family: cursive;
  }
  .back-btn{
    padding-top: 30px;
    grid-area: bb;
  }
  .back-btn button{
    border: 2px solid #49b5e7;
    padding: 5px 15px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 8px;
    font-family: cursive;
  }
  .back-btn button:hover{
    color: white;
    background: #49b5e7;
  }
  .back-btn button:focus{
    outline: none;
  }
  .sub-header{
    grid-area: sh;
    display: flex;
    flex-direction: column;
    background: white;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .sub-header h1{
    color: #32394c;
    font-size: 20px;
  }
  .sub-header h4{
    color: #32394c;
    font-size: 11px;
  }
  .text h1{
    font-size: 15px;
  }
  .inputField h4{
    font-size: 10px;
  }
  .text{
    display: flex;
  }
  .inputField{
    display: flex;
    flex-direction: column;
  }
  .inputField input{
    background: transparent;
    padding: 2px 12px;
    max-width: 205px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  .inputField1 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 200px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField1 h4{
    font-size: 10px;
  }
  .inputField2 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 200px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField2 input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  .inputField2 h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .submit-btn{
    padding-top: 30px;
    grid-area: bb;
  }
  .submit-btn button{
    border: 2px solid #49b5e7;
    padding: 5px 25px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 13px;
    font-family: cursive;
  }
  .submit-btn button:hover{
    color: white;
    background: #49b5e7;
  }
}

/* ipad view */
@media only screen and (min-width: 500px) and (max-width: 900px){
  .signup{
    padding: 0;
    margin: 0;
    width: 100%;
    height: auto;
    display: grid;
    grid-template-rows: 210px 90px 70px 70px 70px 90px 70px 90px;
  }
  .register{
    display: grid;
    grid-template-areas: 
    "mh mh"
    "sh sh"
    "sh sh";
  }
  .main-header{
    grid-area: mh;
    display: grid;
    grid-template-areas: 
    "l l . bb";
  }
  .logo{
    grid-area: l;
  }
  .logo a{
    font-size: 25px;
    color: #32394c;
    font-weight: bold;
    font-family: cursive;
  }
  .back-btn button{
    border: 2px solid #49b5e7;
    padding: 5px 15px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 18px;
    font-family: cursive;
  }
  .back-btn button:hover{
    color: white;
    background: #49b5e7;
  }
  .back-btn{
    padding-top: 25px;
    grid-area: bb;
  }
  .sub-header{
    grid-area: sh;
    display: flex;
    flex-direction: column;
    background: white;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .sub-header h1{
    color: #32394c;
    font-size: 30px;
  }
  .sub-header h4{
    color: #32394c;
    font-size: 11px;
  }
  .inputField h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .inputField2 h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .text h1{
    font-size: 20px;
  }
  .inputField input{
    width: 400px;
    background: transparent;
    padding: 3px 12px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  /*  */
  .inputField1{
    display: flex;
    flex-direction: column;
    grid-area: i1;
  }
  .inputField2{
    display: flex;
    flex-direction: column;
    grid-area: i2;
  }
  .inputs{
    grid-area: i;
    display: grid;
    grid-template-areas:
    "i1 . i2";
  }
  .text{
    display: block;
    grid-area: t;
  }
  .inputField{
    grid-area: if;
    display: flex;
    flex-direction: column;
  }
  .inputField1 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 200px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField1 h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .inputField input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  .inputField2 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 200px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField2 input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
 
  .B-owner{
    padding-top: 20px;
    display: grid;
    grid-template-areas: 
    "t . . i i";
  }
  .B-name{
    display: grid;
    grid-template-areas: 
    "t . . . . . . if";
  }
  .contact{
    display: grid;
    grid-template-areas: 
    "t . . . . . . if";
  }
  .email{
    display: grid;
    grid-template-areas: 
    "t . . . . . . . . . . . if";
  }
  .address{
    padding-top: 20px;
    display: grid;
    grid-template-areas: 
    "t . . . . . i i";
  }
  .B-type{
    display: grid;
    grid-template-areas: 
    "t . . . . . . if";
  }
  .submit{
    /* background: darksalmon; */
    display: grid;
    justify-content: center;
  }
   .submit button{
    border: 2px solid #49b5e7;
    padding: 5px 15px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 18px;
    font-family: cursive;
  }
  .submit button:hover{
    color: white;
    background: #49b5e7;
  }
  
}

/* desktop view */
@media only screen and (min-width: 900px){
  .signup{
    padding: 0;
    margin: 0;
    width: 100%;
    height: auto;
    display: grid;
    grid-template-rows: 210px 90px 70px 70px 70px 90px 70px 90px;
  }
  .register{
    display: grid;
    grid-template-areas: 
    "mh mh"
    "sh sh"
    "sh sh";
  }
  .main-header{
    grid-area: mh;
    display: grid;
    grid-template-areas: 
    "l l . bb";
  }
  .logo{
    grid-area: l;
  }
  .logo a{
    font-size: 30px;
    color: #32394c;
    font-weight: bold;
    font-family: cursive;
  }
  .back-btn button{
    border: 2px solid #49b5e7;
    padding: 5px 15px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 20px;
    font-family: cursive;
  }
  .back-btn button:hover{
    color: white;
    background: #49b5e7;
  }
  .back-btn{
    padding-top: 25px;
    grid-area: bb;
  }
  .sub-header{
    grid-area: sh;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: white;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .sub-header h1{
    color: #32394c;
    font-size: 30px;
  }
  .sub-header h4{
    color: #32394c;
    font-size: 11px;
  }
  .inputField h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .inputField2 h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .text h1{
    font-size: 20px;
  }
  .inputField input{
    width: 750px;
    background: transparent;
    padding: 3px 12px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  .inputField1{
    display: flex;
    flex-direction: column;
    grid-area: i1;
  }
  .inputField2{
    display: flex;
    flex-direction: column;
    grid-area: i2;
  }
  .inputs{
    grid-area: i;
    display: grid;
    grid-template-areas:
    "i1 . i2";
  }
  .text{
    display: block;
    grid-area: t;
  }
  .inputField{
    grid-area: if;
    display: flex;
    flex-direction: column;
  }
  .inputField1 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 300px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField1 h4{
    align-content: flex-start;
    font-size: 10px;
  }
  .inputField input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
  .inputField2 input{
    background: transparent;
    padding: 3px 12px;
    max-width: 300px;
    font-size: 16px;
    height: 25px;
    border: 1px solid #32394c;
    border-radius: 8px;
  }
  .inputField2 input:focus{
    outline: none;
    border: 1px solid #32394c;
    color: #32394c;
  }
 
  .B-owner{
    padding-top: 20px;
    display: grid;
    grid-template-areas: 
    "t i";
  }
  .B-name{
    display: grid;
    grid-template-areas: 
    "t . . . . . . . . . . . . . . . . . . . . if";
  }
  .contact{
    display: grid;
    grid-template-areas: 
    "t . . . . . . . . . . . . if";
  }
  .email{
    display: grid;
    grid-template-areas: 
    "t . . . . . . . . . . . . . . . . . . . . if";
  }
  .address{
    padding-top: 20px;
    display: grid;
    grid-template-areas: 
    "t i";
  }
  .address h1{
    width: 140px;
  }
  .B-type{
    display: grid;
    grid-template-areas: 
    "t . . . . . . . . . . . if";
  }
  .submit{
    display: grid;
    justify-content: center;
  }
   .submit button{
    border: 2px solid #49b5e7;
    padding: 5px 15px;
    color: #49b5e7;
    font-weight: bold;
    border-radius: 10px;
    cursor: pointer;
    background: transparent;
    font-size: 18px;
    font-family: cursive;
  }
  .submit button:hover{
    color: white;
    background: #49b5e7;
  }
}



</style>