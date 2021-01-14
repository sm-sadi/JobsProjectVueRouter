<template>
<h1>Want to work with us ?? </h1>
  <div id="nav">
    <router-link to="/">Home</router-link> 
    <router-link :to="{ name :  'About'}">About</router-link> 
    <router-link :to="{ name : 'jobs'}">Jobs</router-link>
  </div>
  <button @click="redirect">Redirect</button>
  <button @click="back"> Go Back</button>
  <button @click="forward">Go forward</button>
  
  <router-view/>
  
</template>

<script>
export default {
  methods:{
    redirect(){
      // console.log(" i want to redirect ");
      this.$router.push({ name : 'About' })
      
    },
    back(){
      // console.log("i want to go back ");
      this.$router.go(-1)
    },
    forward(){
      // console.log(" i want to go forward");
      this.$router.go(1)
    }
  }
}
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin-left: 15px;
}

#nav a.router-link-exact-active {
  color: #edf5f1;
  background-color: #8000ff;
  padding: 10px;
  border-radius: 4px;
}
button{
  color: #1b1d1c;
  background-color: #d3d3da;
  padding: 10px;
  border-radius: 4px;
  margin-left: 15px;
}

</style>
