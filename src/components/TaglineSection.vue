<template>
  <div class="container my-5">
    <div class="row">
      <div class="col-md-7"><img :src="require('@/assets/main.jpg')" alt="" border="0"></div>
      <div class="col-md-5">
        <h1>Changing the way you receive healtcare.</h1>
          <p class="mt-4">
            Get quick and easy access to medical services with HiveMed. Find doctors, 
            schedule appointments, order medications, and receive remote medical advice and treatment. 
            All from the comfort of your own home. Trust HiveMed for fast and convenient healthcare 
            solutions.
          </p>
          <button type="button" class="btn btn-dark">Get Started</button>
          <button type="button" class="btn btn-light" style="margin-left: 10px;">Learn More</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaglineSection',

}
</script>
 
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin-top: 40px;
  color: black;
  font-family: Helvetica;
  font-weight: bold;
  font-size: 40px;
}
img {
  width: 100%;
  height: 400px;
  border: none;
}

</style>
