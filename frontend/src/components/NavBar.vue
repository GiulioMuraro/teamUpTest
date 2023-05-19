<template>
  <div>
    <div v-if="$route.path == '/'" class="bg-gray-800 h-20 flex justify-center items-center">
      <img src="../images/logo.jpeg" alt="Logo" class="max-h-full max-w-80">
    </div>
    <div v-else class="bg-gray-800 h-20 flex justify-start items-center">
      <img src="../images/logoEnlarged.png" alt="Logo" class="max-h-full max-w-80 ml-20">
      <h1 v-if="$route.path == '/LoginView'" class="text-3xl text-white ml-3">LogIn</h1>
      <h1 v-else-if="$route.path == '/SignUpView'" class="text-3xl text-white ml-3">SignUp</h1>
      <h1 v-else-if="$route.path == '/BookingView'" class="text-3xl text-white ml-3">Booking</h1>
      <h1 v-else-if="$route.path == '/AdminAccountView'" class="text-3xl text-white ml-3">Admin Account</h1>
      <h1 v-else-if="$route.path == '/ProfileView'" class="text-3xl text-white ml-3">Profile</h1>
      <OptionsButton class="ml-auto mr-5"/>
    </div>
  </div>
</template>

<script>

import OptionsButton from './OptionsButton.vue'

export default {
  name: 'NavBar',
  components:{
    OptionsButton
  }
    
  
}

</script>
