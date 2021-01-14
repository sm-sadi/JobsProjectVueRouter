<template>
  <div class="jobs">
    
    <h1> jobs page </h1>
    <div class="firstDi" >
        <div   v-for="job in jobs" :key="job.id" class="jobs">
          <router-link :to="{name : 'jobsDetails' , params: {id : job.id }}">
           <h2 > {{job.title}}</h2>
           
           </router-link>
        </div>
    </div>
  </div>

   

</template>

<script>
export default {
//   name: 'jobs',
//   components: { },
  data(){
      return{
          jobs :[
              {title : 'UX Designer' , id: 1 , detaills : "Lorem, ipsum dolor sit amet"},
              {title : 'Frontend Developer' , id: 2 , detaills : "Lorem, ipsum dolor sit amet"},
              {title : 'Backend Developer' , id: 2 , detaills : "Lorem, ipsum dolor sit amet"}
          ]
      }
  }
}
</script>





<style  scoperd>

.homeimage{
  /* height:8rem;
  width: 10rem; */
  float: left;
  margin: 0px 10px;
}
.firstDiv{
background-color: rgb(223, 231, 238);
padding: 5px 5px;
margin: 0 40px;
}
.homeimage2{
  /* height:8rem;
  width: 10rem; */
  float: right ;
  margin: 0px 10px;
}
.secDiv{
background-color: rgb(243, 219, 223);
padding: 20px 40px;
}
.jobs h2{
  color: rgb(27, 21, 21);
  text-decoration: none;
  padding: 20px;
  background-color: rgb(233, 227, 227);
  width: 50%;
margin : 0 auto 10px;
border-radius: 6px ;
}
.jobs h2:hover{
  color: rgb(239, 238, 245);
  text-decoration: none;
background-color: rgb(36, 33, 33);
 padding: 30px;
  /* background-color: rgb(187, 213, 243); */
}

.jobs a{
  color: rgb(143, 129, 129);
  text-decoration: none;
  background-color: rgb(187, 213, 243);
}


</style>
