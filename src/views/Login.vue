<template>
  <div class="container">
    <section class="vh-100">
  <div class="container-fluid h-custom">
    <p :class="this.currentType"></p>
    <div>
        <div class="form-check form-switch">
            <label for="flexSwitchCheckDefault">{{this.currentType }}</label>
            <input class="form-check-input" type="checkbox" v-on:click="changeStat($event)" id="flexSwitchCheckDefault">
        </div>
    </div>
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col-md-9 col-lg-6 col-xl-5">
        <img src="https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-login-form/draw2.webp"
          class="img-fluid" alt="Sample image">
      </div>
      <div class="col-md-8 col-lg-6 col-xl-4 offset-xl-1">
        <form>

          <!-- Email input -->
          <div class="form-outline mb-4">
            <input type="email" id="form3Example3" class="form-control form-control-lg"
              placeholder="Enter Employee ID" />
            <label class="form-label" for="form3Example3">Employee ID</label>
          </div>

          <!-- Password input -->
          <div class="form-outline mb-3">
            <input type="password" id="form3Example4" class="form-control form-control-lg"
              placeholder="Enter password" />
            <label class="form-label" for="form3Example4">Password</label>
          </div>

          <div class="text-center text-lg-start mt-4 pt-2">
            <button type="button" class="btn btn-primary btn-lg"
              style="padding-left: 2.5rem; padding-right: 2.5rem;">{{this.currentType}}</button>
          </div>

        </form>
      </div>
    </div>
  </div>
  <div
    class="d-flex flex-column flex-md-row text-center text-md-start justify-content-between py-4 px-4 px-xl-5 bg-primary">
    <!-- Copyright -->
    <div class="text-white mb-3 mb-md-0">
      Copyright © 2020. All rights reserved.
    </div>
    <!-- Copyright -->

    <!-- Right -->
    <div>
      <a href="#!" class="text-white me-4">
        <i class="fab fa-facebook-f"></i>
      </a>
      <a href="#!" class="text-white me-4">
        <i class="fab fa-twitter"></i>
      </a>
      <a href="#!" class="text-white me-4">
        <i class="fab fa-google"></i>
      </a>
      <a href="#!" class="text-white">
        <i class="fab fa-linkedin-in"></i>
      </a>
    </div>
    <!-- Right -->
  </div>
</section>
  </div>
</template>

<script>
/* eslint-disable */
export default {
    name:"LoginPage",
    date(){
        return{
            currentType:"Time In",
        };
    },
    methods:{
        changeStat(e){
            console.log(e.target.checked)
            if(e.target.checked){
                this.currentType = "Time Out";
            }
            else {
                this.currentType = "Time In";
            } 
            console.log(this.currentType)
        }
    }
}
</script>

<style scoped>
    .divider:after,
.divider:before {
content: "";
flex: 1;
height: 1px;
background: #eee;
}
.h-custom {
height: calc(100% - 73px);
}
@media (max-width: 450px) {
.h-custom {
height: 100%;
}
}

#flexSwitchCheckDefault {
    width:12rem;
    height:6rem;
}
</style>>
