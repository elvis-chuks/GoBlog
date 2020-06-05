<template>
  <div class="home">
    <main>
      <section class="form">
        <div class="form-top">
          <h1>Welcome to GoBlog</h1>
          <p>Sign Up to start posting articles.</p>
        </div>
        <div class="form-body">
          <form action="#">
            <div class="form-group">
              <label for="password">E-mail address</label>
              <input type="email" class="form-input" id="email" required>
            </div>
            
            <div class="form-group">
              <label for="password">Password</label>
              <input type="password" class="form-input" id="password" required>
            </div>
            <input type="button" value="Sign Up" @click="signUp()">
          </form>
        </div>
        <div class="form-bottom">
          <p>Have an account ?  <router-link tag="a" :to="{name:'Login'}"><strong> Login  </strong> </router-link> </p>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  methods:{
    signUp(){
      console.log('helo')
      this.$router.push({name:'Posts'})
    }
  }
}
</script>

<style scoped>
/* *{
  background:#938B8B;
  height:100%;
} */
main{
  width:50%;
  margin:auto;
  display:flex;
  align-items: center;
  justify-content: center;
  height:100vh;
  
}
input{
  display:block;
}
.form{
  box-shadow: 0px 1px 30px rgba(0, 0, 0, 0.05);
  padding:20px 40px;
  width:60%;
}
.form-top{
  margin-top:40px;
}
.form-top h1{
  font-size:20px;
  font-weight: 500;
}
.form-top p{
  font-size:12px;
  color:grey;
  margin-top:10px;
}
.form-body{
  margin-top:40px;
}
label{
  font-size:10px;
  color:grey;
}
input{
  width:100%;
  border-radius: 5px;
  padding:10px;
  border:1px solid rgba(1, 1, 1, 0.3);

}
.form-group{
  margin-top:20px;
}
.form-bottom{
  margin-top:30px;
  text-align:center;
  margin-bottom:20px;
}
.form-bottom p{
  font-size: 14px;
}


input[type=button]{
  margin-top:40px;
  color:white;
  background:#332A2A;
  border-radius: 3px;
  font-size:12px;
  cursor: pointer;
}

@media(max-width:1024px){
  main{
    width:90%;
  }
  .form{
    width:100%;
  }
}
</style>
