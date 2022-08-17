<template>
 <div>
  <Signin></Signin>
  <!-- <Signup></Signup> -->
 </div>
</template>

<script>
import Signin from './login/signin.vue';
import Signup from './login/signup.vue';
export default {
    components: { Signin, Signup },
}
</script>
