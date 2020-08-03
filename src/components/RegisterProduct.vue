<template>
  <div>
    <div v-if='showRegister'>
      <h3>Register Your Rux!</h3>
      <p>
        Thanks for choosing our 60L Colorway, Other Features Rux
      </p>
      <form @submit='submit'>
        <input type='text' placeholder="First Name"/>
        <input type='text' placeholder="Last Name" />
        <input class='readonly' type='text' readonly='readonly' placeholder="serial" v-model='computedSerial'>
        <input type='text' placeholder="Email" />
        <div class='label-wrapper'>
          <label class='sign-up' for='checkbox'>Sign me up for deals on more equipment from Rux</label>
          <input class='checkbox' type='checkbox' />
        </div>
        <div class='push-down'>
          <button>Register</button>
        </div>

      </form>
    </div>
    <div v-else>
      Your Rux was successfully registered.
    </div>

  </div>
</template>
<script>
  export default {
    name:'RegisterProduct',
    props:['serial'],
    computed: {
      computedSerial: function(){
        return "Serial Number = " + this.serial
      }
    },
    data: ()=>{
      return{
        showRegister:true
      }
    },
    methods:{
      submit: function(e){
        e.preventDefault()
        this.showRegister = false
      }
    }
  }
</script>
<style lang='scss' scoped>
form{
    max-width:480px;
    margin: 0 auto;
    input[type="text"]{
      width:85%;
      padding:20px;
      margin-top:10px;
      margin-bottom: 10px;
      background-color: rgb(235,235,235);
      border:none;

    }
    input[type="checkbox"]{
      width:16px;
      height:16px;
    }
    .readonly{
      color: #adadad;
      cursor: not-allowed;
    }
    label.sign-up{
      font-size:10px;
      margin-right:8px;
    }
    button{
      background-color:rgb(187,57,54);
      color:white;
      border-radius:2px;
      color:rgb(247,247,247);
      padding:0 16px;
      height:45px;
      border:none;
      text-transform:uppercase;
    }
    .push-down{
      margin-top: 10px;
    }
    .label-wrapper{
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
</style>
