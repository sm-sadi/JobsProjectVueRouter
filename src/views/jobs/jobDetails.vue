<template>
  <div v-if="job">
     <h1>job Details Page</h1>
     <p> the job id is - {{ id }}</p>
     <h2> title : {{job.title}}</h2>
     <h4 > <span class="jobDetail">job Description:</span> {{job.details}}</h4>
  
  </div>
  <div v-else>
      <h1>job Details Page</h1>
  
  </div>
</template>

<script>
export default {
    props : [ 'id'],
    data(){
        return{
            // id : this.$route.params.id
            job : null
        }
    },
    mounted(){
        fetch('http://localhost:3000/jobs/' + this.id)
        .then( res => res.json() )
        .then( data => this.job = data)
        .catch( function(err){
          console.log(err);
        })
    }
}
</script>

<style scoped>

.jobDetail{
  color: rgb(121, 70, 238)
}
</style>>

