<template>
  
  
<body>
  
<div class="login-box">
  <h1>Login</h1>
  <div class="textbox">
    <i class="fas fa-user"></i>
    <input type="text" placeholder="Username">
  </div>

  <div class="textbox">
    <i class="fas fa-lock"></i>
    <input type="email" placeholder="e-mail">
  </div>

  <div class="textbox">
    <input type="date" >
  </div>

  <div class="textbox">
    <input type="text" placeholder="Faculdade">
  </div>

  <div class="textbox">
    <input type="text" placeholder="Curso">
  </div>

  <div class="textbox">
    <input type="text" placeholder="Endereço">
  </div>

  <input type="button" class="btn" value="Sign in">
</div>
</body>       
  
  
</template>
<style scoped>

body{
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  background-color: blue;
  /* background-image: url(/assets/foguete-hackathon.jpg) no-repeat; */
  background-size: cover;
}
.login-box{
  width: 280px;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  color: white;
  background-color: rgba(0, 0, 0, 0.7);
}
.login-box h1{
  text-align: center;
  font-size: 40px;
  border-bottom: 6px solid #4caf50;
  margin-bottom: 50px;
  padding: 13px 0;
}
.textbox{
  width: 100%;
  overflow: hidden;
  font-size: 20px;
  padding: 8px 0;
  margin: 8px 0;
  border-bottom: 1px solid #4caf50;
}
.textbox i{
  width: 26px;
  float: left;
  text-align: center;
}
.textbox input{
  border: none;
  outline: none;
  background: none;
  color: white;
  font-size: 18px;
  width: 80%;
  float: left;
  margin: 0 10px;
}
.btn{
  width: 100%;
  background: none;
  border: 2px solid #4caf50;
  color: white;
  padding: 5px;
  font-size: 18px;
  cursor: pointer;
  margin: 12px 0;
}

</style>